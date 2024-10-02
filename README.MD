This is a work on progress ansible playbook for deploying a ceph cluster.

#Complete
Basic playbook for bootstrapping ceph mons on a cluster.

#To-Do

Add tasks to add mgrs.
Add tasks to add osds.
Add tasks to add aux modules (cephfs, samba, nfs, icusi, rgw)
Overhaul playbook structure to make playbook more modular and readable (break up playbooks based on tasks, add handlers for repeating tasks, ect...)

#Instructions

Add designated hostnames and IP addresses to the inventory file.
Add hostnames to the mons.yml based on whether they're initial mons or additional mons.
Make sure that the number of initial+new mons in the mons.yml match the number of hosts in the inventory file.
The playbook will fail if you try to add an even number of mons.
