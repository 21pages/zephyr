cmake_minimum_required(VERSION 3.13.1)
include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(crypto)

target_include_directories(
  app
  PRIVATE
  $ENV{ZEPHYR_BASE}/subsys/net/ip
  $ENV{ZEPHYR_BASE}/subsys/net/l2/ieee802154
  )
FILE(GLOB app_sources src/*.c)
target_sources(app PRIVATE ${app_sources})
