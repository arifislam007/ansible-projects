```bash
---
- name: Facth file from host-1 Ubuntu to Ansible Local
  hosts: web01
  tasks:
    - name: Fatch file
      fetch:
        src: /home/sadmin/host1/index.html #Location of the remote host where actual file stored
        dest: /home/sadmin/files/ #Location of Ansible Host where files will facth from remote host
        flat: yes

- name: Copy file to remote host2
  hosts: svr1
  tasks:
    - name: copy fatched file from host1 to host2
      copy:
       src: /home/sadmin/files/index.html
       dest: /home/sadmin/host2/
```
