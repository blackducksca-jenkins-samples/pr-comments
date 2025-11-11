# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_BlackduckSca_PR_Comments/main`
- **Build Number:** #3
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 1 min 19 sec and counting
- **Timestamp:** 2025-11-11 18:57:20 UTC

---

## Console Output

```
Branch indexing
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from 69c91bdffbf22cdc6ed69126e1d72a4799c5800e
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision e969196a63b1be83b84541b022f7aa52928bd5e5
The recommended git tool is: NONE
using credential Github_Username_PAT
 > git rev-parse --resolve-git-dir /Users/madhusud/.jenkins/workspace/ub_BlackduckSca_PR_Comments_main@libs/a0dda568bac7bbb4a171f59ba3f2660c21c69edc6356524e9ae8bb4500c12bbb/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Fetching without tags
Fetching upstream changes from https://github.com/integrations-garage/blackduck-logs-publisher
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/integrations-garage/blackduck-logs-publisher +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision e969196a63b1be83b84541b022f7aa52928bd5e5 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
Commit message: "Phase 3 - 2"
 > git rev-list --no-walk e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
[Pipeline] Start of Pipeline
[Pipeline] node
Running on mac-sh in /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential Github_Username_PAT
Fetching changes from the remote Git repository
Fetching without tags
 > git rev-parse --resolve-git-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/.git # timeout=10
 > git config remote.origin.url https://github.com/blackducksca-jenkins-samples/pr-comments.git # timeout=10
Fetching upstream changes from https://github.com/blackducksca-jenkins-samples/pr-comments.git
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/blackducksca-jenkins-samples/pr-comments.git +refs/heads/main:refs/remotes/origin/main # timeout=10
Checking out Revision 69c91bdffbf22cdc6ed69126e1d72a4799c5800e (main)
Commit message: "Jenkins log upload - Build #2"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 69c91bdffbf22cdc6ed69126e1d72a4799c5800e # timeout=10
 > git rev-list --no-walk 31879c94fab0de6c6302c8c5afc5bb6e96e5b681 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] script
[Pipeline] {
[Pipeline] echo
JOB_NAME: MBP_Github_BlackduckSca_PR_Comments/main
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm
[Pipeline] {
[Pipeline] sh
+ node --version
v22.16.0
[Pipeline] sh
+ npm --version
10.9.2
[Pipeline] sh
+ npm install
npm warn deprecated fsevents@1.2.9: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.

up to date, audited 1412 packages in 10s

32 packages are looking for funding
  run `npm fund` for details

137 vulnerabilities (9 low, 35 moderate, 57 high, 36 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (blackduck-security-scan)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm
[Pipeline] {
[Pipeline] echo
DETECT_PROJECT_NAME will be set to: MBP_Github_BlackduckSca_PR_Comments
[Pipeline] withEnv
[Pipeline] {
[Pipeline] echo
Workspace is /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main
[Pipeline] security_scan
**************************** START EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_PR_Comments
-------------------------------- Connection to node --------------------------------
[Security Scan] INFO: Jenkins job is running on agent node remotely
-------------------------- Parameter Validation Initiated --------------------------
[Security Scan] INFO:  --- product = [BLACKDUCKSCA]
[Security Scan] INFO: Parameters for blackducksca:
[Security Scan] INFO:  --- blackducksca_waitForScan = true
[Security Scan] INFO:  --- blackducksca_token = ******************************************************************************
[Security Scan] INFO:  --- blackducksca_url = https://saastest.app.blackduck.com
[Security Scan] INFO:  --- blackducksca_prComment_enabled = true
------------------------------------------------------------------------------------
[Security Scan] INFO: Parameters for additional configuration:
[Security Scan] INFO:  --- network_airgap = false
[Security Scan] INFO: Black Duck SCA parameters are validated successfully
[Security Scan] INFO: Bridge download parameters are validated successfully
[Security Scan] INFO: Bridge download is not required. Found installed in: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
------------------------------------------------------------------------------------
[Security Scan] INFO: Bridge CLI version is - 3.9.2
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_PR_Comments
[Security Scan] INFO: Black Duck SCA PR Comment is ignored for non pull request scan
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_PR_Comments
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage blackducksca --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/blackducksca_input9543467212210574473.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-11 18:56:28.7567 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-11 18:56:28.7620 IST [Bridge CLI] INFO: Found version "3.0.143" in registry for workflow "blackducksca", trying to load it from local cache
2025-11-11 18:56:28.8400 IST [Bridge CLI] INFO: Input Resources:
2025-11-11 18:56:28.8400 IST [Bridge CLI] INFO: resource = value [source]
2025-11-11 18:56:28.8400 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-11 18:56:28.8401 IST [Bridge CLI] INFO: blackducksca.token = ***************************************** [blackducksca_input9543467212210574473.json]
2025-11-11 18:56:28.8401 IST [Bridge CLI] INFO: blackducksca.url = https://saastest.app.blackduck.com [blackducksca_input9543467212210574473.json]
2025-11-11 18:56:28.8401 IST [Bridge CLI] INFO: blackducksca.waitForScan = true [blackducksca_input9543467212210574473.json]
2025-11-11 18:56:28.8401 IST [Bridge CLI] INFO: network.airgap = false [blackducksca_input9543467212210574473.json]
2025-11-11 18:56:28.8401 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-11 18:56:28.8401 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca
2025-11-11 18:56:28.8404 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Controller
2025-11-11 18:56:28.8455 IST [Bridge CLI] INFO: Starting Adapter: Default Black Duck SCA Scan Mode
2025-11-11 18:56:28.8496 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-11 18:56:28.8749 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-11 18:56:28.8751 IST [Check pull request] INFO: Adapter finished
2025-11-11 18:56:28.8963 IST [Default Black Duck SCA Scan Mode] INFO: Provided value for resource 'blackducksca.scan.full'
2025-11-11 18:56:28.8965 IST [Default Black Duck SCA Scan Mode] INFO: Adapter finished
2025-11-11 18:56:29.7429 IST [Blackduck SCA Controller] INFO: Found Black Duck SCA Detect jar file "detect-11.0.0.jar" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0"
2025-11-11 18:56:29.7484 IST [Blackduck SCA Controller] INFO: Provided value for resource 'detect.execution.path'
2025-11-11 18:56:29.7485 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-detect
2025-11-11 18:56:29.7485 IST [Bridge CLI] INFO: Starting adapters for stage scm
2025-11-11 18:56:29.7485 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-post-processing
2025-11-11 18:56:29.7493 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Results
2025-11-11 18:56:29.7493 IST [Bridge CLI] INFO: Starting Adapter: Detect Component Locator
2025-11-11 18:56:29.7493 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Detect Execution
2025-11-11 18:56:29.7493 IST [Bridge CLI] INFO: Starting Adapter: SCM Checker
2025-11-11 18:56:29.7495 IST [Blackduck SCA Controller] INFO: Adapter finished
2025-11-11 18:56:29.8218 IST [Blackduck SCA Detect Execution] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect --blackduck.offline.mode=false --blackduck.url=https://saastest.app.blackduck.com --blackduck.api.token= --detect.wait.for.results=true --detect.blackduck.scan.mode=INTELLIGENT
2025-11-11 18:56:30.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect-Self-Updater:  Checking https://saastest.app.blackduck.com/api/tools/detect API for centrally managed Detect version to download to /Users/madhusud/tmp.
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Unable to download jar from https://saastest.app.blackduck.com/api/tools/detect.
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Response code from https://saastest.app.blackduck.com/api/tools/detect was: 400 Bad Request
2025-11-11 18:56:33.4817 IST [Blackduck SCA Detect Execution] INFO: ______     _            _
2025-11-11 18:56:33.4818 IST [Blackduck SCA Detect Execution] INFO: |  _  \   | |          | |
2025-11-11 18:56:33.4818 IST [Blackduck SCA Detect Execution] INFO: | | | |___| |_ ___  ___| |_
2025-11-11 18:56:33.4818 IST [Blackduck SCA Detect Execution] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-11 18:56:33.4818 IST [Blackduck SCA Detect Execution] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-11 18:56:33.4818 IST [Blackduck SCA Detect Execution] INFO: |___/ \___|\__\___|\___|\__|
2025-11-11 18:56:33.4818 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-11 18:56:33.5671 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-11 18:56:33.5672 IST [Blackduck SCA Detect Execution] INFO: Detect Version: 11.0.0
2025-11-11 18:56:33.5672 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Current property values:
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- --property = value [notes]
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.api.token = **************************************************************************************************** [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.offline.mode = false [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.url = https://saastest.app.blackduck.com [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.blackduck.scan.mode = INTELLIGENT [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge [env] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.project.name = MBP_Github_BlackduckSca_PR_Comments [env] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.wait.for.results = true [cmd] 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect build date: 2025-10-30
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-11-13-26-33-559
2025-11-11 18:56:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:56:39.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully connected to Black Duck SCA (version 2025.7.1)!
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Docker tool.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Docker actions finished.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Bazel tool.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Bazel actions finished.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Detectors tool.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Searching for detectors.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detector Report
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm (depth 0)
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/package-lock.json
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/package.json
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detectors actions finished.
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project name: MBP_Github_BlackduckSca_PR_Comments
2025-11-11 18:56:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project version: 1.3.0
2025-11-11 18:56:44.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully completed package manager scan of file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-11 18:56:46.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the codelocation file uploads.
2025-11-11 18:56:50.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] INFO: --- Try #1 for task bdio upload (elapsed: 00:00:00.000)...complete!
2025-11-11 18:56:50.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the codelocation file uploads.
2025-11-11 18:56:50.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:56:50.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Signature Scanner tool.
2025-11-11 18:56:54.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- The Black Duck Signature Scanner downloaded/found successfully: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools
2025-11-11 18:56:54.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No scan targets provided - registering the source path /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm to scan
2025-11-11 18:56:55.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the Black Duck Signature Scan commands.
2025-11-11 18:56:55.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck CLI command: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/jre/Contents/Home/bin/java -Done-jar.silent=true -Done-jar.jar.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/cache/scan.cli.impl-standalone.jar -Xmx4096m -jar /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/scan.cli-1.0.6-standalone.jar --no-prompt --scheme https --host saastest.app.blackduck.com --port 443 -v --logDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-11-13-26-33-559/scan/BlackDuckScanOutput/2025-11-11_13-26-55-713_1 --statusWriteDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-11-13-26-33-559/scan/BlackDuckScanOutput/2025-11-11_13-26-55-713_1 --project MBP_Github_BlackduckSca_PR_Comments --release 1.3.0 --name nodejs-npm/MBP_Github_BlackduckSca_PR_Comments/1.3.0 signature --exclude /node_modules/ --exclude /.bridge/ --scass-scan /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- 
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck Signature Scanner return code: 0
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Signature Scanner log output directory: '/Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-11-13-26-33-559/scan/BlackDuckScanOutput/2025-11-11_13-26-55-713_1'
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the Black Duck Signature Scan commands.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature Scanner actions finished.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Binary Scanner tool.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary scanner found nothing to upload.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary Scanner actions finished.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Container Scanner tool.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No detect.container.scan.file.path property was provided. Skipping container scan.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Container Scanner actions finished.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- IaC Scanner tool will not be run.
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-11 18:57:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/38202d46-441b-414e-8d55-f6db06c945a5/versions/3087ad1c-cbf3-43a3-b386-05e9a6f2dd1b/bom-status/de90a8d5-569d-45f5-b720-51f716114584 (elapsed: 00:00:00.000)...complete!
2025-11-11 18:57:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/38202d46-441b-414e-8d55-f6db06c945a5/versions/3087ad1c-cbf3-43a3-b386-05e9a6f2dd1b/bom-status/83fb03a9-1514-4fe1-b0cc-343cceb7596f (elapsed: 00:00:00.000)...not done yet, waiting 1 seconds and trying again...
2025-11-11 18:57:08.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #2 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/38202d46-441b-414e-8d55-f6db06c945a5/versions/3087ad1c-cbf3-43a3-b386-05e9a6f2dd1b/bom-status/83fb03a9-1514-4fe1-b0cc-343cceb7596f (elapsed: 00:00:01.754)...not done yet, waiting 2 seconds and trying again...
2025-11-11 18:57:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #3 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/38202d46-441b-414e-8d55-f6db06c945a5/versions/3087ad1c-cbf3-43a3-b386-05e9a6f2dd1b/bom-status/83fb03a9-1514-4fe1-b0cc-343cceb7596f (elapsed: 00:00:04.501)...not done yet, waiting 3 seconds and trying again...
2025-11-11 18:57:14.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #4 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/38202d46-441b-414e-8d55-f6db06c945a5/versions/3087ad1c-cbf3-43a3-b386-05e9a6f2dd1b/bom-status/83fb03a9-1514-4fe1-b0cc-343cceb7596f (elapsed: 00:00:08.247)...complete!
2025-11-11 18:57:14.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Checking to see if Detect should check policy for violations.
2025-11-11 18:57:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-11-13-26-33-559/status/status.json
2025-11-11 18:57:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Result ========
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Black Duck SCA Project BOM: https://saastest.app.blackduck.com/api/projects/38202d46-441b-414e-8d55-f6db06c945a5/versions/3087ad1c-cbf3-43a3-b386-05e9a6f2dd1b/components
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Status ========
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- NPM: SUCCESS
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature scan / Snippet scan on /Users/madhusud/Jenkins_Testing/Nodes/workspace/ub_BlackduckSca_PR_Comments_main/nodejs-npm: SUCCESS
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ===============================
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-11 18:57:16.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect duration: 00h 00m 46s 038ms
2025-11-11 18:57:16.3876 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.completed'
2025-11-11 18:57:16.3877 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.results.path'
2025-11-11 18:57:16.3879 IST [Blackduck SCA Detect Execution] INFO: Adapter finished
2025-11-11 18:57:16.4223 IST [Blackduck SCA Results] INFO: Skipping Blackduck SCA issues retrieval as "blackducksca.fixpr.enabled" is configured to false
2025-11-11 18:57:16.4291 IST [Blackduck SCA Results] INFO: Adapter finished
2025-11-11 18:57:16.4717 IST [SCM Checker] INFO: Provided value for resource 'jenkins.enabled'
2025-11-11 18:57:16.4717 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-policy-violations-fetcher
2025-11-11 18:57:16.4722 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Policy Violations Fetcher
2025-11-11 18:57:16.4724 IST [SCM Checker] INFO: Adapter finished
2025-11-11 18:57:16.4952 IST [Detect Component Locator] INFO: skipping fix pull requests creation as "blackducksca.fixpr.enabled" is configured to false
2025-11-11 18:57:16.5000 IST [Detect Component Locator] INFO: Adapter finished
2025-11-11 18:57:16.5325 IST [Blackduck SCA Policy Violations Fetcher] INFO: Detected Intelligent scan, will fetch Intelligent scan policy violations data
2025-11-11 18:57:17.5643 IST [Blackduck SCA Policy Violations Fetcher] INFO: Bearer token retrieved successfully
2025-11-11 18:57:17.9082 IST [Blackduck SCA Policy Violations Fetcher] INFO: Project data retrieved successfully
2025-11-11 18:57:18.2762 IST [Blackduck SCA Policy Violations Fetcher] INFO: Version data retrieved successfully
2025-11-11 18:57:18.6317 IST [Blackduck SCA Policy Violations Fetcher] INFO: Detected 5 policy violations
2025-11-11 18:57:19.0171 IST [Blackduck SCA Policy Violations Fetcher] INFO: Added entry to resource 'blackducksca.policy.rules.violations'
2025-11-11 18:57:19.0174 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.minor'
2025-11-11 18:57:19.0175 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.blocker'
2025-11-11 18:57:19.0177 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.trivial'
2025-11-11 18:57:19.0178 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.unspecified'
2025-11-11 18:57:19.0180 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.major'
2025-11-11 18:57:19.0182 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.critical'
2025-11-11 18:57:19.0184 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.ok'
2025-11-11 18:57:19.0186 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.projectBomUrl'
2025-11-11 18:57:19.0190 IST [Blackduck SCA Policy Violations Fetcher] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Total issues found: 1095
[Security Scan] INFO: Security Scan execution is successful
**************************** END EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Black Duck Logs Publisher - Starting log upload process
[Pipeline] echo
Configuration: [githubOrg:blackducksca-jenkins-samples, repoName:pr-comments, credentialsId:github-pat-logs-publisher, maxRetries:3, retentionCount:5, jobNamePrefixes:[MBP_Github_, MBP_, Github_, Pipeline_, Job_, Build_]]
[Pipeline] echo
Job Name: MBP_Github_BlackduckSca_PR_Comments/main
[Pipeline] echo
Build Number: 3
[Pipeline] echo
GitHub Organization: blackducksca-jenkins-samples
[Pipeline] withCredentials
Masking supported pattern matches of $GITHUB_TOKEN
[Pipeline] {
[Pipeline] echo
Using configured repository name: pr-comments
[Pipeline] echo
Target repository: blackducksca-jenkins-samples/pr-comments
[Pipeline] echo
LogProcessor: captureJenkinsLogs called
```

---

*Log generated by Black Duck Logs Publisher*