# 🚗 Cyber Automotive Security - Anomaly Detection System

## **Descrição do Projeto**
Este projeto foi desenvolvido para proteger redes CAN bus de veículos contra ataques cibernéticos, utilizando Inteligência Artificial avançada. O sistema emprega um **Autoencoder** para detecção de anomalias em tempo real, capaz de identificar comportamentos incomuns nos componentes do veículo. Nossa solução é embarcada, funcionando localmente em um computador de bordo, como o Raspberry Pi, sem depender de redes externas.

## **Objetivo**
Detectar e prevenir ataques cibernéticos em veículos conectados, oferecendo uma solução robusta, eficiente e escalável para montadoras automotivas.

## **Tecnologias Utilizadas**
- **Hardware**: 
  - Raspberry Pi
  - Arduino
- **Software**: 
  - Python (TensorFlow/Keras, Scikit-learn, CAN)
  - Rede CAN bus simulada
- **IA**: 
  - Autoencoder não supervisionado
- **Frameworks e Bibliotecas**: 
  - TensorFlow/Keras para desenvolvimento do modelo
  - MinMaxScaler para normalização de dados
  - Python-can para comunicação com a rede CAN

## **Funcionalidades**
- **Detecção de Anomalias**: Identificação de padrões anormais no comportamento do veículo.
- **Sistema Embarcado**: Processamento local no Raspberry Pi, eliminando a necessidade de redes externas.
- **Simulação CAN bus**: Testes realizados em uma rede CAN simulada para validação prática.
- **Operação em Tempo Real**: Capacidade de monitoramento contínuo com alto desempenho.

## **Como Funciona**
1. **Entrada de Dados**: 
   - Dados como velocidade do motor, torque e posição do acelerador são recebidos via CAN bus.
2. **Pré-processamento**: 
   - Os dados são normalizados utilizando o mesmo scaler do treinamento.
3. **Inferência com Autoencoder**: 
   - O Autoencoder reconstrói os dados normais e calcula o erro de reconstrução.
4. **Detecção de Anomalia**: 
   - Caso o erro de reconstrução exceda um limiar predefinido, uma anomalia é sinalizada.
5. **Feedback**: 
   - Resultados são exibidos no terminal indicando se os dados são normais ou anômalos.

## **Como Executar**
### **Pré-requisitos**
- Raspberry Pi com Python instalado.
- Arduino configurado para simular a rede CAN bus.
- Modelo treinado (`autoencoder_model.keras`) e scaler de normalização.

### **Passos**
1. Clone o repositório:
   git clone https://github.com/seu_usuario/seu_repositorio.git

2. Navegue para o diretório do projeto:
   cd seu_repositorio

3. Instale as dependências:
   pip install -r requirements.txt

4. Configure a interface CAN bus no Raspberry Pi.

5. Execute o script principal:
python main.py