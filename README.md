# aws-firewall-stacks
AWS CloudFormation

# Insights Gerais - Firewall e CloudFormation

1. **Infraestrutura como Código (IaC)**: CloudFormation transforma configurações manuais em templates reutilizáveis.
2. **Reusabilidade**: Componentes como Security Groups e Roles devem ser definidos em recursos separados.
3. **Idempotência**: Reexecutar a stack não duplica recursos — apenas aplica mudanças necessárias.
4. **Segurança**: Sempre limitar o IP de acesso SSH (nunca abrir para 0.0.0.0/0).
5. **Automação**: `UserData` é ideal para instalar serviços simples; para setups complexos, usar o **AWS Systems Manager** ou **Ansible**.
6. **Debug**: Logs de inicialização ficam em `/var/log/cloud-init-output.log` na instância.

# Principais aprendizados

Criação de instâncias EC2 declarando recursos com AWS::EC2::Instance.

Automação da configuração de servidores com UserData (instalação do Apache e criação de página HTML).

Uso de Fn::Base64 e !Sub para executar scripts e incluir variáveis dinâmicas.

Criação e associação de Security Groups para controlar o tráfego (portas 22 e 80).

Execução de stacks via AWS CLI (create-stack, describe-stacks, delete-stack).

Boas práticas de segurança, como restringir acesso SSH e organizar os recursos por função.

# Insights

CloudFormation reduz erros manuais e padroniza implantações.

Separar cada recurso em seu próprio template facilita manutenção e reuso.

A documentação e os testes são partes essenciais do aprendizado contínuo.

