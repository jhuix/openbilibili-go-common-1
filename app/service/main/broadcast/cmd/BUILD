package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "cmd",
    embed = [":go_default_library"],
    tags = ["automanaged"],
)

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "go-common/app/service/main/broadcast/cmd",
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
    deps = [
        "//app/service/main/broadcast/server/grpc:go_default_library",
        "//app/service/main/broadcast/server/http:go_default_library",
        "//app/service/main/broadcast/service:go_default_library",
        "//library/conf/env:go_default_library",
        "//library/conf/paladin:go_default_library",
        "//library/ecode/tip:go_default_library",
        "//library/log:go_default_library",
        "//library/naming:go_default_library",
        "//library/naming/discovery:go_default_library",
        "//library/net/ip:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
