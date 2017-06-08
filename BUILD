cc_library(
    name = "catch",
    srcs = ["catch.hpp"],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "main",
    srcs = ["main.cpp"],
    linkstatic = True,
    visibility = ["//visibility:public"],
    deps = [":catch"],
    alwayslink = True,
)
