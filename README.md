# Network_cisco
repositorio para anotar comandos do packet tracer
## COMANDOS BÁSICOS  
enable  
conf t    
copy running-config startup-config  
wr  
### adicionando senhas  
`enable secreat <senha_secreta>`  
line console 0   
`password <senha_console>`    
login  
## comando switch  
### criando vlan  
vlan id  
EX: vlan 10
name vlan_name
EX: name vlan10
show vlan brief -> mostra as vlans existentes

### criando o trunk  
interface gig0/0    
switchport mode trunk  
show interface trunk  


### setando as vlan  
interface range fa0/1-8   
switchport access vlan 10    
  
### colocando um ip na vlan  
` interface vlan <id>`  
`ip address <ip> <submask>`  

### definindo o gateway padrão  
`ip default-gateway <ip_gateway>`  
   
   
## comando router  
### Subredes    
interface gig0/0.1 -> entrando na subnet   
encapsulation dot1Q vlan_id native -> EX: encapsulation dot1Q  10 native  
ip addresses IP SUBMASK  

### DHCP  
ip dhcp pool nome_pool  
network IP SUBMASK  
default-router IP_GATEWAY  
ip dhcp excluded-address IP_Inicio IP_FIM -> EX: ip dhcp excluded-address 192.168.10.1 192.168.10.9  
### RIP
  para que o rip aconteça precisamos digitar os seguintes comandos no rip    
  `router rip`  
  `network <rede>` -> devemos subistituir <rede> pela rede que desejamos adicionar no rip  
  nota: podemos adicionar quantos networks quisermos
  
 
## subredes
  
  ![image](https://user-images.githubusercontent.com/101679723/230175244-5b6a898e-fb4e-4d7f-a8d0-816fe9053cca.png)  
  subredes comuns:
  /24 256 ips 254 hosts uteis, utilizada por redes domesticas comuns
  /30 4 ips 2 hosts uteis, muito utilizada para fazer redes entre roteadores

