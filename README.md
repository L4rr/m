# Ansible Vagrant profile for AWX

## Background

## Getting Started

ansible -m ping servers -i ./hosts 
ansible -m shell -a 'free -m'  servers -i ./hosts 



## run

ansible-galaxy install -r requirements.yml

ansible-playbook -i ./hosts -l servers provisioning/playbook.yml 

git commit -m "Removing useless sip.conf configurations since we just need pjsip.conf. Sip is the old version, pjsip is the new standard and they work in parallel. Now we configured every device (twilio and extensions) to all work just with pjsip. \nFurther documentation https://www.linkedin.com/pulse/faqs-sip-vs-chansip-chanpjsip-kent-adams"

## debugging

sudo tcpdump -nqt -s 0 -A -i eth0 port 5060

