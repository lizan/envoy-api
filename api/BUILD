load("//bazel:api_build_system.bzl", "api_proto_library")

api_proto_library(
    name = "address",
    srcs = ["address.proto"],
)

api_proto_library(
    name = "base",
    srcs = ["base.proto"],
    deps = [":address"],
)

api_proto_library(
    name = "health_check",
    srcs = ["health_check.proto"],
    deps = [":base"],
)

api_proto_library(
    name = "tls_context",
    srcs = ["tls_context.proto"],
)

api_proto_library(
    name = "cds",
    srcs = ["cds.proto"],
    deps = [
        ":address",
        ":base",
        ":health_check",
        ":tls_context",
    ],
    has_services = 1,
)

api_proto_library(
    name = "eds",
    srcs = ["eds.proto"],
    deps = [
        ":address",
        ":base",
        ":health_check",
    ],
    has_services = 1,
)

api_proto_library(
    name = "hds",
    srcs = ["hds.proto"],
    deps = [
        ":base",
        ":health_check",
    ],
    has_services = 1,
)

api_proto_library(
    name = "lds",
    srcs = ["lds.proto"],
    deps = [
        ":address",
        ":base",
        ":tls_context",
    ],
    has_services = 1,
)

api_proto_library(
    name = "rds",
    srcs = ["rds.proto"],
    deps = [":base"],
    has_services = 1,
)
