package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "config.go",
        "diff.go",
        "fileinfo.go",
        "generator.go",
        "kazel.go",
        "proto.go",
        "sourcerer.go",
    ],
    importpath = "github.com/hawkingrei/kazel/kazel",
    deps = [
        "//kazel/util/sets:go_default_library",
        "//vendor/github.com/bazelbuild/buildtools/build:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
    ],
)

go_binary(
    name = "kazel",
    embed = [":go_default_library"],
)
