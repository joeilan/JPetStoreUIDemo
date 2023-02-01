pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Get some code from a GitHub repository
                git url: 'https://github.com/joeilan/JPetStoreUIDemo.git', branch: 'main'
                
            }
        }
        stage('Functional Test - HCL OneTest UI') {
            steps {
                echo("************************** Functional Test - HCL OneTest UI Start **************************")
                step([$class: 'RTWProductHelper', configfile: '', exportReportFileName: '', exportReportFolder: '', exportReportFormat: '', exportReportType: 'unified', exportReportUsage: false, exportstatreportlist: '', exportstats: '', exportstatsformat: '', exportstatshtml: '', imports: '', imsharedloc: '', labels: '', name: 'HOTUIDemo', overwrite: 'true', project: 'JPetStore', protocolinput: '', publish: '', publishfor: '', publishreports: '', quiet: 'false', results: '', suite: 'Tests\\PlaceOrderFish.testsuite', swapdatasets: '', usercomments: '', varfile: '', vmargs: '', workspace: 'C:\\Users\\ilangathirj\\git\\JPetStoreUIDemo'])

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}


