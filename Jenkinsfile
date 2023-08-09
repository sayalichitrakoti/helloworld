pipeline:
  agent:
    any

  stages:
    - stage: Checkout
      steps:
        - checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/sayalichitrakoti/helloworld.git']]])

    - stage: Build
      steps:
        - bat 'mvn clean package'
