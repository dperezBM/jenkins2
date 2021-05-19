pipeline
{
	agent any
	stages {
		stage('compilar') {
			steps {
				echo "Estoy compilando el codigo de Sprint Boot"
				sh './mvnw compile'
			}
		}
		stage('test') {
			steps {
				echo "Estoy probando el codigo de Sprint Boot"
				sh './mvnw test'
			}
		}
		stage('package') {
			steps {
				echo "Estoy generando el JAR del proyecto"
				sh './mvnw package'
			}
		}
		stage('deploy') {
			steps {
				echo "Estoy desplegando a /tmp del servidor Jenkins"
				sh 'cp target/calculadora-0.0.1-SNAPSHOT.jar /tmp'
			}
		}

	}

}
