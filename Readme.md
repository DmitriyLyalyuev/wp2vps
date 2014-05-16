First run
=========

    $ ansible-playbook -i hosts <playbook>.yml -kK

Or you may use one node
=======================

    $ ansible-playbook -i hosts <playbook>.yml -l host0.example.org -kK

Second and other runs not need use -kK keys
===========================================

    $ ansible-playbook -i hosts <playbook>.yml

    $ ansible-playbook -i hosts <playbook>.yml -l host0.example.org
