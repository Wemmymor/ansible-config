# ansible-config
#testing......
finally able to ping all the servers after trying for 9 days.....insane right.
# save artifacts.


Jenkinsfile for quick task
============================
```
pipeline {
    agent any

  stages {
     stage('Initial CleanUp') {
      steps {
        dir("${WORKSPACE}") {
          deleteDir()
        }
      }
    }

    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }

    stage('Package') {
      steps {
        script {
          sh 'echo "Packaging Stage"'
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          sh 'echo "Deploying Stage"'
        }
      }
    }

    stage('Clean up') {
      steps {
        script {
          sh 'echo "Cleaning up Stage"'
        }
      }
    }
    }
}

