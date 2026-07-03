# Setup Pós-Formatação — Windows 11 25H2

Checklist de configuração para máquinas com Windows 11 25H2, incluindo ajustes de sistema, GPO e uma correção específica para o notebook Acer Nitro V.

## Índice

- [1. Windows 11 25H2](#1-windows-11-25h2)
- [2. Política de Grupo (Gpedit)](#2-política-de-grupo-gpedit)
- [3. Acer Nitro V — Boot Device not found](#3-acer-nitro-v--boot-device-not-found)

---

## 1. Windows 11 25H2

- [ ] Desativar o Windows Defender
- [ ] Desativar o Controle Inteligente de Aplicativo (Smart App Control)
- [ ] Desativar o Proxy
- [ ] Desativar sugestões do Windows:
  `Configurações > Sistema > Notificações > desmarcar "Sugestões do Windows"`
- [ ] Instalar drivers:
  1. Driver Intel
  2. Driver NVIDIA
- [ ] Conferir a taxa de atualização (Hertz Monitor)

## 2. Política de Grupo (Gpedit)

Desabilitar atualizações automáticas via Editor de Política de Grupo Local.

**Passo a passo:**

1. `Iniciar` → `gpedit.msc`
2. `Configuração do Computador`
3. `Modelos Administrativos`
4. `Componentes do Windows`
5. `Windows Update`
6. `Gerenciar a Experiência do Usuário Final`
7. `Configurar Atualizações Automáticas`
8. Definir como **Desabilitado**

## 3. Acer Nitro V — Boot Device not found

**Sintoma:** o notebook exibe a mensagem `Boot Device not found` ao ligar.

**Solução:** entrar na BIOS e desabilitar o **VMD Controller**.

**Passo a passo:**

1. Ligar o notebook e entrar na BIOS (tecla `F2` ou `Del` durante o boot)
2. Localizar a opção **VMD Controller**
3. Desabilitar
4. Salvar e sair (`F10`)
