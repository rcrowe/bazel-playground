load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "event.go",
        "main.go",
    ],
    importpath = "github.com/utilitywarehouse/partner-bazel-hello/api/verification/cmd/verification",
    visibility = ["//visibility:private"],
    deps = [
        "//api/account/pkg/cuba:go_default_library",
        "@com_github_utilitywarehouse_partner_pkg_event//:go_default_library",
        "@com_github_utilitywarehouse_partner_pkg_operational//:go_default_library",
    ],
)

go_binary(
    name = "verification",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["cmd_test.go"],
    embed = [":go_default_library"],
)
