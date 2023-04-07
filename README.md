Test CI locally using Act on a Mac.

## Usage

Step 1: [Install Act](https://github.com/nektos/act#installation)

    $ brew brew install act

Step 2: [Run github-act-cache-server](https://github.com/sp-ricard-valverde/github-act-cache-server#run)

    $ git clone https://github.com/sp-ricard-valverde/github-act-cache-server
    $ cd github-act-cache-server
    $ docker compose up --build
    $ ACT_CACHE_AUTH_KEY=foo docker compose up --build

Step 3: Run!

    $ git clone https://github.com/wojtekmach/test_ci
    $ cd test_ci
    $ act

To use your Mac as the runnner, run:

    $ act -P ubuntu-22.04=-self-hosted

Run Linux/x64 on an Apple Sillicon Mac: (OTP 23 is the last release before JIT by default)

    $ act --container-architecture linux/amd64 --env ARCH=x86_64 --env OTP_VERSION=23.3

## License

Copyright (c) 2023 Wojtek Mach

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
