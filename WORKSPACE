load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_java",
    sha256 = "7c4bbe11e41c61212a5cf16d9aafaddade3f5b1b6c8bf94270d78215fafd4007",
    strip_prefix = "rules_java-c13e3ead84afb95f81fbddfade2749d8ba7cb77f",
    urls = [
        "https://github.com/bazelbuild/rules_java/archive/c13e3ead84afb95f81fbddfade2749d8ba7cb77f.tar.gz",
    ],
)

http_archive(
    name = "com_google_elemental2",
    strip_prefix = "elemental2-master",
    url = "https://github.com/google/elemental2/archive/master.zip",
)

load("@com_google_elemental2//build_defs:repository.bzl", "load_elemental2_repo_deps")

load_elemental2_repo_deps()

load("@com_google_elemental2//build_defs:workspace.bzl", "setup_elemental2_workspace")

setup_elemental2_workspace()

http_archive(
    name = "com_google_j2cl",
    strip_prefix = "j2cl-master",
    url = "https://github.com/google/j2cl/archive/master.zip",
)

load("@com_google_j2cl//build_defs:repository.bzl", "load_j2cl_repo_deps")

load_j2cl_repo_deps()

load("@com_google_j2cl//build_defs:rules.bzl", "setup_j2cl_workspace")

setup_j2cl_workspace()

load("//third_party/maven_utils:maven.bzl", "setup_maven")

setup_maven()

load("//third_party/maven_utils:maven_install.bzl", "install_maven")

install_maven()

load("@maven//:compat.bzl", "compat_repositories")

compat_repositories()

load("//third_party/protobuf:protobuf.bzl", "setup_protobuf")

setup_protobuf()

load("//third_party/protobuf:protobuf_install.bzl", "install_protobuf")

install_protobuf()

http_archive(
    name = "com_google_j2cl_protobuf",
    strip_prefix = "j2cl-protobuf-fixes",
    url = "https://github.com/Project-Godel/j2cl-protobuf/archive/fixes.zip",
)

load("@com_google_j2cl_protobuf//:repository.bzl", "load_j2cl_proto_repo_deps")

load_j2cl_proto_repo_deps()
