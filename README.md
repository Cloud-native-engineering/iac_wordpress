# iac_wordpress

This project uses cloud-init and Ansible to automate the process of installing and configuring WordPress and a database. By using these tools, we can create a repeatable and reliable process for deploying WordPress on a variety of cloud platforms and environments. Our automation includes the installation of a web server, PHP, a MariaDB database server, and the WordPress software. With this automated deployment process, we can quickly and easily deploy new instances of WordPress and ensure they are configured correctly and securely.

## Cloud-init

This project includes two cloud-init files. The first one is written using run-commands, while the second one is implemented using the cc-ansible role, which is supported by cloud-init.

The cloud-init file that uses the run-commands module is designed to execute a series of shell commands during the initialization process. This method is useful for simple configuration tasks, such as installing packages, configuring network settings, or creating user accounts.

On the other hand, the cloud-init file that uses the cc-ansible role is implemented using Ansible, which is a popular configuration management tool. The cc-ansible module enables users to write Ansible playbooks and execute them as part of the cloud-init initialization process. This method is more powerful and flexible than run-commands since Ansible allows for more complex configuration tasks, such as configuring databases, deploying applications, or managing infrastructure.

| File-name                                | ansible managed    | run-commands       | ansible role       |
|------------------------------------------|--------------------|--------------------|--------------------|
| [cloud-init-cmd](cloud-init-cmd)         | :white_check_mark: | :white_check_mark: |         :x:        |
| [cloud-init-ansible](cloud-init-ansible) | :white_check_mark: |         :x:        | :white_check_mark: |

> I recommend you use the version that uses the Ansible module within cloud-init. It is easier to understand and manage.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the [LICENSE](LICENSE) file for details.

## Author Information

This code was created in 2023 by [Yves Wetter](mailto:yves.wetter@edu.tbz.ch).
