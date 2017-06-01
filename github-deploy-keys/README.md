# ansible-github-deploy-keys
Ansilbe role to install github deploy keys

## Role Variables

Available variables are listed below, along with default values:

    github_deploy_keys_key_title: "Ansilbe auto generated"
    github_deploy_keys_key_path: ~/.ssh/id_rsa.pub  # key file to use as the deploy key
    github_deploy_keys_read_only: false  # set this to true to make the deploy key read only
    github_deploy_keys_github_user:  # username of the owner of the remote repo
    github_deploy_keys_github_repo:  # repo name of the remote repo
    github_deploy_keys_github_access_token:  # github access_token previously obtained

## Example Playbook

    - hosts: webservers
      roles:
        - { role: kasun.github-deploy-keys, github_deploy_keys_github_user: 'kasun', github_deploy_keys_github_user: 'my-repo',
            github_deploy_keys_github_access_token: "{{ github_access_token }}",
            github_deploy_keys_key_path: "/home/user/.ssh/id_rsa.pub" }

## License

MIT
