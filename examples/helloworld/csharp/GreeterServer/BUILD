load("@io_bazel_rules_dotnet//dotnet:csharp.bzl", "csharp_binary")
load("@org_pubref_rules_protobuf//csharp:rules.bzl", "csharp_proto_library")

csharp_binary(
    name = "GreeterServer",
    srcs = [
        "Program.cs",
    ],
    deps = [
        ":Helloworld",
        "@nuget_google_protobuf//:libnet45",
        "@nuget_grpc//:core",
        "@nuget_grpc//:runtime_osx",
        "@nuget_grpc//:system_interactive_async",
    ],
)

csharp_proto_library(
    name = "Helloworld",
    proto_deps = [
        "//proto:csharp",
    ],
    protos = ["//helloworld/proto:protos"],
    verbose = 0,
    with_grpc = True,
)
