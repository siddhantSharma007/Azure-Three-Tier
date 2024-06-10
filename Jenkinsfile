pipeline {
    agent any
    stages {
        stage('Input') {
            steps {
                script {
                    def userInput = input(
                        id: 'userInput', message: 'Provide parameters', parameters: [
                            string(name: 'NAME', defaultValue: 'World', description: 'Who should be greeted?'),
                            booleanParam(name: 'USE_POLITE_GREETING', defaultValue: true, description: 'Should the greeting be polite?')
                        ]
                    )
                    echo "Hello, ${userInput.NAME}!"
                    if (userInput.USE_POLITE_GREETING) {
                        echo "Nice to meet you!"
                    } else {
                        echo "How are you?"
                    }
                }
            }
        }
    }
}
