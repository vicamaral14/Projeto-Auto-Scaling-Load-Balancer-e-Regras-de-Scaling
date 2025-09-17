# Projeto-Auto-Scaling-Load-Balancer-e-Regras-de-Scaling
## 📖 Sobre o Projeto

Este repositório tem como objetivo documentar de forma simples e prática os conceitos de Auto Scaling, Load Balancer e regras de Scaling Up e Down, explicando o que são, o que foi aprendido e exemplos de passos para configuração.

## ⚙️ O que é cada serviço?

🔹 Auto Scaling

Serviço que ajusta automaticamente a quantidade de instâncias (máquinas virtuais) de acordo com a demanda.
  - Garante alta disponibilidade.
  - Evita custos desnecessários.
```bash
ex: Imagina que você tem uma lanchonete.
  - Se chega muita gente ao mesmo tempo, você precisa de mais funcionários para atender.
  - Se fica vazio, você manda alguns para casa para não gastar dinheiro à toa.
- É isso que o Auto Scaling faz: ele aumenta ou diminui a quantidade de “funcionários virtuais” (máquinas/servidores) de acordo com o movimento.
````

🔹 Load Balancer

Balanceador de carga que distribui as requisições entre várias instâncias.
  - Evita sobrecarga de uma única máquina.
  - Melhora a experiência do usuário.
```bash
Ex: Agora imagina que você tem vários caixas na sua lanchonete.
Se todo mundo for para o mesmo caixa, vai ter fila e demora. O Load Balancer é como um gerente que organiza a fila e manda cada cliente para um caixa diferente, deixando tudo equilibrado e rápido.
```

🔹 Regras de Scaling (Up & Down)
  - Scaling Up: adicionar instâncias quando a demanda aumenta.
  - Scaling Down: remover instâncias quando a demanda cai.

```bash
EX: Essas regras são como combinados que você faz:
  - Scaling Up (para cima): “Se tiver mais de 10 clientes na fila, chamo mais um funcionário”.
  - Scaling Down (para baixo): “Se não tiver quase ninguém, libero um funcionário para descansar”.
Na tecnologia é a mesma coisa: o sistema cria ou desliga máquinas dependendo do uso.
`````

## 📚 O que aprendemos
  - Auto Scaling e Load Balancer trabalham em conjunto para manter um sistema estável.
  - É necessário planejar regras de escalabilidade com métricas bem definidas.
  - Essas práticas trazem elasticidade e economia em ambientes de nuvem.
  - Ferramentas de monitoramento (como CloudWatch) são fundamentais.

-----
## 🛠️ Passo a passo simplificado
✅ Auto Scaling
  - Criar instância base.
  - Configurar Launch Template.
  - Criar Auto Scaling Group definindo limites (mínimo, máximo, desejado).
  - Conectar ao CloudWatch para monitoramento.

✅ Load Balancer
  - Escolher o tipo (ex.: Application Load Balancer).
  - Definir as instâncias/ASG que receberão tráfego.
  - Configurar listeners e portas (80/443).
  - Testar o acesso pelo DNS do Load Balancer.

✅ Regras de Scaling
  - Criar alarmes no CloudWatch, por exemplo:
  - CPU > 70% → Scaling Up.
  - CPU < 30% → Scaling Down.
  - Definir cooldown (tempo de espera entre escalonamentos).
  - Validar com testes de carga.

## 📌 Conclusão
Este projeto mostrou que o uso conjunto de Auto Scaling e Load Balancer traz resiliência, escalabilidade e economia de custos para sistemas em nuvem. Além disso, as regras de scaling up e down são essenciais para ajustar os recursos de forma inteligente.
