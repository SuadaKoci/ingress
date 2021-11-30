pipeline{

	agent any

	stages {
		stage ('Helm deploy'){
			steps {
					sh ("/usr/local/bin/helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx")
					sh ("/usr/local/bin/helm repo update")
				
			}
		}
		stage ('Kubernetis deploy'){
			steps {
					sh ("/usr/local/bin/kubectl apply -f ingress.yaml")
				
			}
		}
	}

}
