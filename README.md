# Comandos
Comandos utilizados
---
title: Comandos
author: Celina Pacheco Cruz
date: 2024-10-01
category: Jekyll
layout: post
---
## Configuracion IP
### Configurando las IP del Router:

```bash
Router>enable
Router#config t
Router(config)#hostname CBA
Cba(config)#interface gig0/0
Cba(config-if)#ip address 70.80.0.1 255.240.0.0
Cba(config-if)> no shutdown
Cba(config-if)> exit
Cba(config)> exit
Cba(config)#interface se0/3/1
Cba(config-if)#ip address 70.64.0.1 255.240.0.0
Cba(config-if)> no shutdown
Cba(config-if)> exit
Cba(config)> exit
Cba(config)#interface Se0/3/0
Cba(config-if)#ip address 70.16.0.1 255.240.0.0
Cba(config-if)> no shutdown
Cba(config-if)> exit
Cba(config)> exit
Cba# write
```
### Configurando la computadora:
Para la respectiva configuracion de la computadora se pone Desktop/ip Configuration y se rellenan los siguientes campos:
1. IPv4 Address 
2. Subnet Mask
3. Default Gateway

## Rutas Dinamicas
### Configuracion de Rutas dinamicas
```bash
colca# show ip interface
colca# config t
colca(config)# router eigrp 10
colca(config-router)#network 70.96.0.0
colca(config-router)#network 70.80.0.0
colca(config-router)#exit
```
## VLAN
### Configuracion de VLAN
```bash
switch>enable
switch# config t
switch(config)> vlan 10
switch(config-vlan)> name Ventas
switch(config-vlan)> exit
switch(config)> vlan 20
switch(config-vlan)> name Finanzas
switch(config-vlan)> exit
switch# show vlan brief
switch# write
```

