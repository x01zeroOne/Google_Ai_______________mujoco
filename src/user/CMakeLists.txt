# Copyright 2021 DeepMind Technologies Limited
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

set(MUJOCO_USER_SRCS
    user_api.cc
    user_api.h
    user_composite.cc
    user_composite.h
    user_flexcomp.cc
    user_flexcomp.h
    user_init.cc
    user_mesh.cc
    user_model.cc
    user_model.h
    user_objects.cc
    user_objects.h
    user_util.cc
    user_util.h
)

target_sources(mujoco PRIVATE ${MUJOCO_USER_SRCS})
target_compile_definitions(mujoco PRIVATE MUJOCO_TINYOBJLOADER_IMPL)
