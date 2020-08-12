# ansible-inventory
IaC ansible demo (https://factory.southbridge.io/issues/365841)
## technical notes
Reset cource:
```sh
git rm --cached hosts/main files/deploy_key/id_*
vim group_vars/all.yml # base_zsh_enable: False
vim group_vars/runners.yml # deploy_db_host: "{{ groups['db']|first }}"
                           # cleanup runner_reg_token
vim hosts/pgcluster # comment out
```
