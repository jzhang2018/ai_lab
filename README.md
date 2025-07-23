# ai_lab
A Workstation VM lab to practice agentic ai topics. The lab is built on VMWare Workstation Red Hat 9 Linux VM. </br>
The VM requires: 16G RAM, 4 CPU core and 60G hard disk. </br>

The Local LLM stack specs: </br>
- Ollama: lightweight LLM runner (runtime / framework) </br>
- Codellama(7b-instruct): LLM, CPU friendly </br>
- Smol-developer: agent library </br>
- Open WebUI: Browser based user prompt with connection to Ollama </br>

Usefull links: </br>
- Ollama url: http://<YOUR_VM_IP>:11434 </br>
- Open WebUI: http://<YOUR_VM_IP>:3000 </br>

Playbooks: </br>
- If you have to expand your VM hard disk, you need to run this resize playbook first: </br>
ansible-playbook -i inventories/hosts.yml playbooks/resize_root_lvm.yml </br>
- Run following playbook to build a local LLM stack. It might take about 10~15 min: </br>
ansible-playbook -i inventories/hosts.yml playbooks/local_llm_stack.yml </br>