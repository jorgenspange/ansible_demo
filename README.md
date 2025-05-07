Prerequisites:
--------------
  - Configure IP to hosts inventory (inventory/host_vars/..)

Ansible Variable Precedence:
----------------------------
| Precedence | Source |
|------------|--------|
| 1 | Command line values (e.g., `-u my_user`; not variables) |
| 2 | Role defaults (`role/defaults/main.yml`) |
| 3 | Inventory file or script group vars |
| 4 | `inventory/group_vars/all` |
| 5 | `playbook/group_vars/all` |
| 6 | `inventory/group_vars/*` |
| 7 | `playbook/group_vars/*` |
| 8 | Inventory file or script host vars |
| 9 | `inventory/host_vars/*` |
| 10 | `playbook/host_vars/*` |
| 11 | Host facts / cached `set_facts` |
| 12 | Play vars |
| 13 | `vars_prompt` (in play) |
| 14 | `vars_files` (in play) |
| 15 | Role vars (`role/vars/main.yml`) |
| 16 | Block vars (only for tasks in block) |
| 17 | Task vars (only for the task) |
| 18 | `include_vars` |
| 19 | `set_facts` / registered vars |
| 20 | Role (`include_role`) parameters |
| 21 | Include parameters |
| 22 | Extra vars (`--extra-vars`, always win) |
