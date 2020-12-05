node{
stage("Prepare Run Environment"){
cleanWs()
}

stage("Clone from GIT Repo"){
sh 'git clone https://github.com/slmeghana/GeneralSpringBootProgExce.git'
}

stage("Execute sequencer file for Build and Deployment")
{
executeAnsiblePlaybookAsStages([playbookFile: sequencer_file, inventoryFile: hosts_file])
}
sequencer_file="GeneralSpringBootProgExce/ansible/sequencer.yml"
hosts_file="GeneralSpringBootProgExce/ansible/hosts"
}
