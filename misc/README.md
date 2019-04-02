# Things to know about ansible

1) You can pass parameters to roles

2) To make the command module idempotent, use "creates"
   ansible will run the command only when creates location have the
   pattern defined

3) Using Ansible setup’s module to gather information about your hosts
    $ ansible localhost -m setup

4) You can list all tasks of a playbook
    ansible-playbook install-apache.yml --list-tasks

5) Use ansible-vault when you want to store sensitive information

6) Using with_items, Some modules handle collections of items really
   well and are actually faster than running the same task multiple
   times with different parameters.

7) Use Local_Actions,Sometimes you might want to run a task on your
   local machine instead of running it on the remote machine.

8) You can tell Ansible to run a task only once "run_once: true"

9) Ansible supports running a playbook in dry run mode. Ansible will
   not make any changes to your host, but simply report what changed

10) Tasks can be run step-by-step "--step"

11) Tasks can be run based on their tags
    --tags <tagname> (or simply -t) and --skip-tags <tagnames>
