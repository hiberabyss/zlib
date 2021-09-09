load("@rules_foreign_cc//foreign_cc:defs.bzl", "configure_make")

filegroup(
  name = "all_srcs",
  srcs = glob([
    "**",
  ])
)

configure_make(
  name = "libz_make",
  # configure_command = "config",
  lib_source = ":all_srcs",
  visibility = ["//visibility:public"],
  out_static_libs = [
    "libz.a",
  ],
)

cc_library(
  name = 'libz',
  deps = [
    ':libz_make',
  ],
  visibility = ["//visibility:public"],
)
