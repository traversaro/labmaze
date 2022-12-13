# Copyright 2019 DeepMind Technologies Limited.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# ============================================================================

workspace(name = "labmaze")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "bazel_skylib",
    sha256 = "4756ab3ec46d94d99e5ed685d2d24aece484015e45af303eb3a11cab3cdc2e71",
    strip_prefix = "bazel-skylib-1.3.0",
    url = "https://github.com/bazelbuild/bazel-skylib/archive/1.3.0.zip",
)

new_local_repository(
    name = "com_google_absl",
    path = "/home/traversaro/mambaforge/envs/labmazedev/include",  # absl placeholder
    build_file = "@//bazel:system_absl.BUILD"
)

http_archive(
    name = "com_google_googletest",
    sha256 = "24564e3b712d3eb30ac9a85d92f7d720f60cc0173730ac166f27dda7fed76cb2",
    strip_prefix = "googletest-release-1.12.1",
    url = "https://github.com/google/googletest/archive/release-1.12.1.zip",
)

new_local_repository(
    name = "pybind11",
    path = "/home/traversaro/mambaforge/envs/labmazedev/include",  # pybind11 placeholder
    build_file = "@//bazel:system_pybind11.BUILD"
)

new_local_repository(
    name = "python_headers",
    path = "/home/traversaro/mambaforge/envs/labmazedev",  # May be overwritten by setup.py.
    build_file = "@//bazel:python_headers.BUILD"
)

load("@bazel_skylib//:workspace.bzl", "bazel_skylib_workspace")
bazel_skylib_workspace()
