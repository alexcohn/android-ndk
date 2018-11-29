cmake_minimum_required(VERSION 3.1.0)
project(buildtest)

message("BUILDING CMAKE TEST PROJECT")

add_library(buildtest SHARED test.c)
