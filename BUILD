load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")
load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:prefix github.com/jschaf/gazelle-go-proto-bug
gazelle(name = "gazelle")

go_library(
    name = "gazelle-go-proto-bug_lib",
    srcs = ["main.go"],
    importpath = "github.com/jschaf/gazelle-go-proto-bug",
    visibility = ["//visibility:private"],
    deps = ["//pgpb"],
)

go_binary(
    name = "gazelle-go-proto-bug",
    embed = [":gazelle-go-proto-bug_lib"],
    visibility = ["//visibility:public"],
)
