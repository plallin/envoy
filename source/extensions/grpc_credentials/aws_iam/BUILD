licenses(["notice"])  # Apache 2

# AWS IAM gRPC Credentials

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "config",
    srcs = ["config.cc"],
    hdrs = ["config.h"],
    external_deps = ["grpc"],
    deps = [
        "//include/envoy/grpc:google_grpc_creds_interface",
        "//include/envoy/registry",
        "//source/common/common:assert_lib",
        "//source/common/config:utility_lib",
        "//source/common/grpc:google_grpc_creds_lib",
        "//source/common/http:message_lib",
        "//source/common/http:utility_lib",
        "//source/extensions/filters/http/common/aws:credentials_provider_impl_lib",
        "//source/extensions/filters/http/common/aws:region_provider_impl_lib",
        "//source/extensions/filters/http/common/aws:signer_impl_lib",
        "//source/extensions/filters/http/common/aws:utility_lib",
        "//source/extensions/grpc_credentials:well_known_names",
        "@envoy_api//envoy/config/grpc_credential/v2alpha:pkg_cc_proto",
    ],
)
