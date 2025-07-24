# 🚀 Início Rápido: Criar uma Máquina Virtual Windows no Portal do Azure

Este guia mostra como criar rapidamente uma máquina virtual (VM) com Windows Server 2022 Datacenter usando o Portal do Azure.

## 🧭 Pré-requisitos
- Conta no Azure (crie uma gratuita se necessário)
- Acesso ao [Portal do Azure](https://portal.azure.com)

## 🛠️ Etapas para Criar a VM

1. **Entrar no Portal**
   - Acesse o [Portal do Azure](https://portal.azure.com)

2. **Criar a Máquina Virtual**
   - Pesquise por “Máquinas Virtuais” e selecione a opção
   - Clique em **Criar > Máquina Virtual do Azure**
   - Configure:
     - Nome: `myVM`
     - Imagem: `Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2`
     - Usuário: `azureuser`
     - Senha: mínimo 12 caracteres com complexidade
     - Regras de porta: habilite RDP (3389) e HTTP (80)
   - Clique em **Examinar + Criar**, depois em **Criar**

3. **Conectar via RDP**
   - Vá para a VM criada e selecione **Conectar > RDP**
   - Baixe o arquivo `.rdp` e abra-o
   - Use as credenciais configuradas para acessar

4. **Instalar o IIS (Servidor Web)**
   - No PowerShell da VM, execute:
     ```powershell
     Install-WindowsFeature -name Web-Server -IncludeManagementTools
     ```

5. **Verificar o IIS**
   - Copie o IP público da VM e cole no navegador
   - A página de boas-vindas do IIS deve aparecer

## 🧹 Limpeza de Recursos

- Para excluir a VM e seus recursos:
  - Vá ao grupo de recursos da VM
  - Clique em **Excluir grupo de recursos**

## ⏱️ Desligamento Automático

- Configure o desligamento automático para evitar cobranças:
  - Na seção **Operações**, selecione **Desligamento automático**
  - Defina o horário e salve

## 📚 Próximos Passos

Explore mais tutoriais sobre VMs no Azure:
- [Tutorial com PowerShell](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/tutorial-manage-vm)
- [Visão geral das VMs](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/overview)

> ⚠️ Este guia é destinado a fins educacionais e não para ambientes de produção.

---

📄 Fonte: [Documentação Oficial Microsoft Learn](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
