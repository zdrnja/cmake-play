cmake_minimum_required(VERSION 3.10)

add_compile_options(
  -Wall
  -Wextra
  -Wpedantic
  -pie
  -fpie
  -O3
)

add_executable (
  changeMyKey
  demo.c
  aes256.c
)
