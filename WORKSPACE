workspace(name = "ctc_sampling")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_google_absl",
    strip_prefix = "abseil-cpp-master",
    urls = ["https://github.com/abseil/abseil-cpp/archive/master.zip"],
)

git_repository(
    name = "openfst",
    commit = "22867ee7b483598a729abe125da2517584a5d010",  # 1.7.2 plus Bazel
    remote = "https://github.com/mjansche/openfst.git",
    shallow_since = "1556726789 +0100",
)
