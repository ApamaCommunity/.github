# GitHub Action sample workflow

See https://github.com/ApamaCommunity/.github/blob/main/workflow-templates/apama.yml for a starter workflow you can 
copy into your repo's `.github/workflows/` directory to add the ability to build and test your Apama applications 
with GitHub Actions. 

This workflow includes:

* installing Apama Community Edition on both Windows and Linux using the https://github.com/ApamaCommunity/github-action-setup-apama action
* building ApamaDoc HTML from your Apama EPL files and publishing it to your repo's gh-pages branch
* building C++ and Java plug-ins
* executing a suite of PySys tests
* uploading an EPL coverage coverage zip (on success) or a zip of test output directories (on failure)

Note that the Linux environment usually executes quite a lot faster than the Windows one, so if you don't need 
multi-platform testing, use a workflow that runs only on Linux for maximum efficiency. You should also delete the 
steps you don't need - especially the steps for setting up the environment for C++ building on Windows which is quite 
time-consuming. 

# License

Installing Apama Community Edition using the setup-apama action in this workflow implies agreement to the 
terms and conditions; see https://cumulocity.com/docs/legal-notices/license-terms-and-conditions/

This workflow sample is:

	Copyright (C) 2020-present Cumulocity GmbH

	Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
	Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

