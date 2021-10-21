# AnsibleCreatingUserWithAZKeyVaultIntegration

1. There are two file name "usercreation_keyvault.yml" and "externalvariable.yml"
   - file "usercreation_keyvault.yml" contain all the configuration and setting related to user making.
   - file "externalvariable.yml" contain all the values need to run the playbook
       - which contain username , group name and credential to authenticate az vault
  2. After specifying all the value we can run our playbook by following command-
  

    ansible-playbook -i hosts usercreation_keyvault.yml --skip-tags delete-user
3. There is need to skip tag delete-user tag because this playbook can delete user also
