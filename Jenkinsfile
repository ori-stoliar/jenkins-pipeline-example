#!groovy

// Define your high level variables per repository
env.CD_SERVICE_NAME = 'foo'
env.CD_REGISTRY = 'xx.xx.xxx'
env.CD_IMAGE_NAME = 'bar'

// Define your variables per branch
def envs = [dev: [someList: "item1,item2,item3,item4,item5",
                      someParameter: "X"],
            stage: [someList: "items3,item4,item5",
                      someParameter: "Y"],
            prod: [someList: "items3,item4,item5",
                      someParameter: "Z"]          ]

library('jenkins-shared-library-example@master') _
buildSomeApp(currentBuild, envs."${env.BRANCH_NAME}")