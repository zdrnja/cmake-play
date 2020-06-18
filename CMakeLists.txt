cmake_minimum_required(VERSION 3.10)

add_compile_options(
  -Wall
  -Wextra
  -Wpedantic
  -pie
  -fpie
  -O3
)

project(simple)

add_executable (
  changeMyKey
  demo.c
  aes256.c
)

add_custom_command(
  OUTPUT final.solution
  COMMAND upx changeMyKey -o x86_64.compressed.dynamic.binary
  COMMENT "Fuck"
  VERBATIM
)

add_custom_target(
  Last_Target ALL
  DEPENDS final.solution
)
