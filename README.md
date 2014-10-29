ansible-cron
============

Tool to run ansible on repo update

Why?
=====

0. Automatically run ansible on commit to git repo
0. Monitor atomated run status: when it was last run and what was last status
0. Current Ansible pull aproach was found as not handy - it needs ansible install and playbooks checkout on every node

Monitoring
==========
/tmp/ansible_status is used for monitoring. Two metrics are used:

0. File timestamp - how much time has gone since last script run
0. File contents should be "ok". If it's not - something happened.
