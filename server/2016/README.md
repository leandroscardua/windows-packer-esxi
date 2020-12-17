Utiliza o packer para criar uma imagem customizada do Windows Server 2016 no ESXI ( Versão Gratuita )

 Programas:
--------
- Sistema Operacional : Linux
- Packer : v1.6.5
- ESXI: 6.7.0 Update 3 (Build 17167734)
- Ovftool: 4.4.0 (build-16360108)

 Requerimentos:
--------
- Habilitar SSH no ESXI
- Habilitar GuestIPHack no ESXI ( https://www.packer.io/docs/builders/vmware/iso#building-on-a-remote-vsphere-hypervisor )
- Instalar o Ovftool no Linux ( https://code.vmware.com/tool/ovf )

 Arquivos:
--------

    .
    ├── ws2019.json                   # arquivo de configuração do packer
    ├── variables.json                # arquivo de configuração para conectar no ESXI
    └── Autounattend.xml              # arquivo para fazer a instalação automatica do windows.
     
 Execucao:
--------

    packer build -var-file variables.json ws2016.json
