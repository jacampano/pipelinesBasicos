pipeline {
    agent any
    stages {
        stage('Example') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                //submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
        stage('Example2') {
            options {
                timeout(time: 5, unit: 'MINUTES') 
            }
            steps {
                script {
                    env.USER_INPUT = input(
                    message: "Selecciona",
                    //submitter: equipo,
                    parameters: [
                        [$class: 'ChoiceParameterDefinition',
                            choices: ['Si','No'].join('\n'),
                            name: 'Continuar',
                            description: 'Seleccionar opción']
                            ])
                }
                
            
                    echo "Se ha seleccionado ${env.USER_INPUT}"
            }
        }
    }
}
