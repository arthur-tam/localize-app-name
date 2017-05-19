<!--
# license: Licensed to the Apache Software Foundation (ASF) under one
#         or more contributor license agreements.  See the NOTICE file
#         distributed with this work for additional information
#         regarding copyright ownership.  The ASF licenses this file
#         to you under the Apache License, Version 2.0 (the
#         "License"); you may not use this file except in compliance
#         with the License.  You may obtain a copy of the License at
#
#           http://www.apache.org/licenses/LICENSE-2.0
#
#         Unless required by applicable law or agreed to in writing,
#         software distributed under the License is distributed on an
#         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#         KIND, either express or implied.  See the License for the
#         specific language governing permissions and limitations
#         under the License.
-->

# localize-app-name

This plugin provides a way to localize your app name

Android:
add the corresponding language folders to locales/android other than the appname default locale (the default appname will set in XDK project Build Settings)

iOS:
add the corresponding language folders to locales/ios (the default appname will set in XDK project Build Settings)

### Supported Platforms

- Android
- iOS

### Example

e.g. if appname default in zh-TW, with additional zh-CN and en locale, then

Step 1: Enter plugin.xml with
```xml
  <!-- android -->
  <platform name="android">
    <resource-file src="locales/android/values-en/strings.xml" target="res/values-en/strings.xml" />
    <resource-file src="locales/android/values-zh-rCN/strings.xml" target="res/values-zh-rCN/strings.xml" />
  </platform>

  <!-- ios -->
  <platform name="ios">
    <resource-file src="locales/ios/en.lproj" />
    <resource-file src="locales/ios/zh-hant.lproj" />
    <resource-file src="locales/ios/zh-hans.lproj" />
  </platform>
```
Step 2: Edit strings.xml/InfoPlist.strings to your appname

