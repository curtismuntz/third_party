workspace(name = "rules_foreign_cc_usage_example")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Group the sources of the library so that CMake rule have access to it
all_content = """filegroup(name = "all", srcs = glob(["**"]), visibility = ["//visibility:public"])"""

# Rule repository
http_archive(
    name = "rules_foreign_cc",
    strip_prefix = "rules_foreign_cc-master",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/master.zip",
)

load("@rules_foreign_cc//:workspace_definitions.bzl", "rules_foreign_cc_dependencies")

# Workspace initialization function; includes repositories needed by rules_foreign_cc,
# and creates some utilities for the host operating system
rules_foreign_cc_dependencies()
# http_archive(
#    name = "opencv_archive",
#    build_file_content = all_content,
#    strip_prefix = "opencv-4.0.0",
#    urls = ["https://github.com/opencv/opencv/archive/4.0.0.tar.gz"],
# )

http_archive(
    name = "opencv_archive",
    build_file_content = all_content,
    strip_prefix = "opencv-3.4.4",
    urls = ["https://github.com/opencv/opencv/archive/3.4.4.tar.gz"],
)

http_archive(
    name = "zlib_archive",
    build_file_content = all_content,
    sha256 = "4ff941449631ace0d4d203e3483be9dbc9da454084111f97ea0a2114e19bf066",
    strip_prefix = "zlib-1.2.11",
    urls = [
        "https://zlib.net/zlib-1.2.11.tar.xz",
    ],
)

http_archive(
    name = "libpng_archive",
    build_file_content = all_content,
    sha256 = "2f1e960d92ce3b3abd03d06dfec9637dfbd22febf107a536b44f7a47c60659f6",
    strip_prefix = "libpng-1.6.34",
    urls = [
        "http://ftp-osl.osuosl.org/pub/libpng/src/libpng16/libpng-1.6.34.tar.xz",
    ],
)
