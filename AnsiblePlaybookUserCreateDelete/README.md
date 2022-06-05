To execute user creation and deletion playbook keep tag in mind 
This playbook delete user also

So to create user use 

## ansible-playbook -i hosts userCreateAndDelete.yml --private-key /home/{USERNAME}/.ssh/id_rsa --skip-tags delete-user

To delete user use

## ansible-playbook -i hosts userCreateAndDelete.yml --private-key /home/{USERNAME}/.ssh/id_rsa --skip-tags "make-user,ssh-key,delete-pub"

The public key path will be

## key="{{ lookup('file', 'userPubKeys/{{ username }}.pub') }}" 


