pipeline{
	agent any
	stages{
		stage('1-clone'){
			when{
				branch 'feature'
			}
			steps{
				sh 'action'
			}
		}
		stage('2-parallel-jobs'){
			when{
				branch 'dev'
			}
			parallel{
				stage('1-saada-subjob1'){
					steps{
						sh 'lscpu'
					}
				}
				stage('2-aubin-subjob2'){
					steps{
						sh 'du -h'
						sh 'df -h'
					}
				}
			}
		}
	}
}