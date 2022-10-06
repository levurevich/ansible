jenkins_master
=========

Deploy jenkins linux master in DevSecOps GPN DevZone environment
After install u need to unlock Jenkins admin by changing /jkfs/jenkins/config.xml flag <useSecurity>true</useSecurity> to false.
Default jenkins new local admin user - dso-admin, with pass in secret place.

Jenkins version {{ latest }}
U can get list of installed plugins by exec script on the jenkins page - http://<jenkins_host>:8080/script

Jenkins.instance.pluginManager.plugins.each{
  plugin -> 
    println ("${plugin.getDisplayName()} (${plugin.getShortName()}): ${plugin.getVersion()}")
}

Plugins installed by plugin-manager-tool except jenkins-ptai-plugin, jenkins-jira-plugin.
There are two install manually

Requirements
------------

sudo enabled user

