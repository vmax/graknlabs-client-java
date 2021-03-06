#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#

package(default_visibility = ["//test/behaviour/graql/language/define:__subpackages__"])
load("@graknlabs_dependencies//tool/checkstyle:rules.bzl", "checkstyle_test")

java_library(
    name = "steps",
    srcs = [
        "GraqlSteps.java"
    ],
    deps = [
        # Package dependencies
        "//test/behaviour/connection:steps",
        "//:client-java",

        # Grakn Labs dependencies
        "@graknlabs_graql//java:graql",

        # External dependencies from Maven
        "@maven//:junit_junit",
        "@maven//:io_cucumber_cucumber_java",
        "@maven//:com_google_guava_guava",
    ],
    visibility = ["//visibility:public"],
)

checkstyle_test(
    name = "checkstyle",
    targets = [
        ":steps",
    ],
    license_type = "apache"
)
