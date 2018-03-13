load("@org_pubref_rules_protobuf//java:deps.bzl", "DEPS")


java_test(
    name = "netty_test",
    size = "small",
    srcs = ["HelloWorldClientTest.java"],
    tags = ["exclusive"],
    test_class = "org.pubref.rules_protobuf.examples.helloworld.client.HelloWorldClientTest",
    runtime_deps = [
        "@org_pubref_rules_protobuf//java:netty_runtime_deps",
    ],
    deps = [
        ":client",
        "//helloworld/java/org/pubref/rules_protobuf/examples/helloworld/server",
        "@junit_junit_4//jar",
    ],
)

java_binary(
    name = "netty",
    main_class = "org.pubref.rules_protobuf.examples.helloworld.client.HelloWorldClient",
    runtime_deps = [
        ":client",
        "@org_pubref_rules_protobuf//java:netty_runtime_deps",
    ],
)

java_library(
    name = "client",
    srcs = ["HelloWorldClient.java"],
    deps = [
        # This rule automatically exports //java:grpc_compiletime_deps.
        "//helloworld/proto:java",
    ],
)
