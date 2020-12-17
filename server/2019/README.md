
Utilizando packer para criar uma imagem customizada no ESXI ( Versao Gratuita )

# Programas:
--------
- Sistema Operacional : Linux
- Packer : v1.6.5
- ESXI: 6.7.0 Update 3 (Build 17167734)
- Ovftool: 4.4.0 (build-16360108)


# Requerimentos:
--------
- Habilitar SSH no ESXI
- Habilitar GuestIPHack no ESXI ( https://www.packer.io/docs/builders/vmware/iso#building-on-a-remote-vsphere-hypervisor )
- Instalar o Ovftool no Linux ( https://code.vmware.com/tool/ovf )

# Arquivos:
--------

    .
    ├── build                   # Compiled files (alternatively `dist`)
    ├── docs                    # Documentation files (alternatively `doc`)
    ├── src                     # Source files (alternatively `lib` or `app`)
    └── README.md


# Execucao:
--------
    packer build -var-file variables.json ws2019.json
