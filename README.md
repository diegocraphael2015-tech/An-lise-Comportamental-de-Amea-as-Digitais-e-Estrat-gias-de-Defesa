# 🛡️ Análise de Ameaças Digitais e Estratégias de Defesa

Repositório técnico desenvolvido para o desafio de cibersegurança da **DIO (Digital Innovation One)**, com foco no estudo conceitual do funcionamento de ameaças digitais (Ransomware e Spyware/Keylogger) e na estruturação de defesas em profundidade.

---

## 📌 Visão Geral do Projeto

O objetivo deste projeto é documentar e analisar os mecanismos de ação de softwares maliciosos comumente observados no cenário de segurança da informação, compreendendo como essas ameaças operam para projetar contramedidas eficazes de prevenção, detecção e resposta a incidentes.

---

## 🔬 Análise de Ameaças

### 1. Ransomware (Criptoameaças)
* **Mecanismo de Ação:** Utiliza algoritmos de criptografia simétrica (ex: AES) para cifrar dados em alta velocidade, combinados com criptografia assimétrica (ex: RSA) para proteger a chave simétrica sem expor o segredo localmente.
* **Vetor de Entrada:** Frequentemente distribuído através de *phishing*, anexos maliciosos, exploração de vulnerabilidades em serviços expostos (RDP, VPNs desatualizadas) ou infecções em cadeia.
* **Impacto:** Indisponibilidade de sistemas críticos, perda de integridade de dados e extorsão digital.

### 2. Keyloggers e Spyware (Interceptação de Entradas)
* **Mecanismo de Ação:** Monitora rotinas de entrada do sistema operacional (ex: interceptação de chamadas de API ou *hooks* de teclado) para registrar digitação de credenciais e dados sensíveis.
* **Canais de Exfiltração:** Envio periódico dos registros capturados via protocolos de rede (HTTP/HTTPS, SMTP ou DNS tunneling).
* **Impacto:** Vazamento de credenciais de acesso, espionagem industrial e quebra de confidencialidade de contas com privilégios.

---

## 🛡️ Medidas de Prevenção, Detecção e Mitigação

A segurança contra ameaças avançadas exige uma abordagem de **Defesa em Profundidade (Defense-in-Depth)**:

| Camada | Tecnologia / Medida | Função |
| :--- | :--- | :--- |
| **Endpoint** | EDR / Antivírus de Próxima Geração (NGAV) | Detecção de comportamento anômalo (ex: múltiplos acessos e renomeação rápida de arquivos). |
| **Identidade** | Princípio do Menor Privilégio (PoLP) | Usuários padrão sem privilégios de administrador para impedir execução de rotinas globais de sistema. |
| **Backup** | Estratégia de Backup 3-2-1 com Imutabilidade | 3 cópias, 2 mídias diferentes, 1 cópia *offsite* (ou imutável / *air-gapped*) imune a criptografia. |
| **Rede** | Firewall e Sandboxing | Inspeção e detecção de arquivos suspeitos antes da entrega aos usuários e bloqueio de portas de comando e controle (C2). |
| **Humana** | Programas de Conscientização em Segurança | Treinamento contínuo contra engenharia social, phishing e abertura de anexos desconhecidos. |

---

## ⚖️ Declaração Ética
Todo o conteúdo deste projeto foi desenvolvido estritamente para propósitos acadêmicos e educacionais, visando a capacitação em defesa cibernética e mitigação de vulnerabilidades.
