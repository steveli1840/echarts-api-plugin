# ECharts Jenkins Plugin

[![Jenkins Version](https://img.shields.io/badge/Jenkins-2.138.4-green.svg?label=min.%20Jenkins)](https://jenkins.io/download/)
![JDK8](https://img.shields.io/badge/jdk-8-yellow.svg?label=min.%20JDK)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Provides [ECharts](https://echarts.apache.org/en/index.html) for Jenkins Plugins.

This plugin contains the latest [WebJars](https://www.webjars.org) release and corresponding Jenkins UI elements. 

## How to use the plugin

In order to use this JS library, add a maven dependency to your pom:
```xml
<dependency>
  <groupId>io.jenkins.plugins</groupId>
  <artifactId>echarts-api</artifactId>
  <version>[latest version]</version>
</dependency>
```

Then you can use ECharts in your jelly files using the following snippet:
```xml
<st:adjunct includes="io.jenkins.plugins.echarts"/>
```
If you don't need all charts, you can also use one of
```xml
<st:adjunct includes="io.jenkins.plugins.echarts-common"/>
<st:adjunct includes="io.jenkins.plugins.echarts-simple"/>
```
which provide smaller .js files, but also fewer charts. See the [echarts documentation](https://echarts.apache.org/en/tutorial.html#Create%20Custom%20Build%20of%20ECharts)
for more information.
 
:info: The underlying Java model of the charts is located in a different module, so it can be re-used in
a non-Jenkins context as well. The source code (MIT license as well) is available in the associated 
[ECharts build trend charts API](https://github.com/uhafner/echarts-build-trends) module.
 
You can find several examples of Jenkins views that use ECharts in the 
[Warnings Next Generation plugin](https://github.com/jenkinsci/warnings-ng-plugin) and in the 
[Forensics plugin](https://github.com/jenkinsci/forensics-api-plugin). There is also a 
[user guide](https://github.com/jenkinsci/forensics-api-plugin/etc/PluginGuide.adoc) 
under progress that introduces the additional classes and concepts. 

[![Jenkins](https://ci.jenkins.io/job/Plugins/job/echarts-api-plugin/job/master/badge/icon)](https://ci.jenkins.io/job/Plugins/job/echarts-api-plugin/job/master/)
[![GitHub Actions](https://github.com/jenkinsci/echarts-api-plugin/workflows/GitHub%20Actions/badge.svg)](https://github.com/jenkinsci/echarts-api-plugin/actions)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/6956fdd7b6ca494c8f07694a18fc3091)](https://www.codacy.com/manual/uhafner/echarts-api-plugin?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=jenkinsci/echarts-api-plugin&amp;utm_campaign=Badge_Grade)
[![Codecov](https://img.shields.io/codecov/c/github/jenkinsci/echarts-api-plugin.svg)](https://codecov.io/gh/jenkinsci/echarts-api-plugin)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/jenkinsci/echarts-api-plugin.svg)](https://github.com/jenkinsci/echarts-api-plugin/pulls)
