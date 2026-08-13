# AXIS VIGILIA: Sistema Inteligente de Monitorização e Reabilitação Postural

> "Um colete que age. Uma tecnologia que pensa."
> Wearable inteligente para correção postural ativa, focado em adolescentes e pacientes em fase pós-colete ortopédico.

## Sobre o Projeto
O **Axis Vigilia** é um projeto multidisciplinar desenvolvido no âmbito do Projeto Integrador em Engenharia Biomédica (Universidade do Minho). 

O dispositivo visa colmatar uma lacuna clínica grave: a falta de acompanhamento contínuo de pacientes após a remoção de coletes ortopédicos rígidos (elevado risco de recaída da escoliose idiopática) e a alta prevalência de alterações posturais em adolescentes.

Diferente das opções comerciais passivas, o Axis Vigilia introduz o conceito de **correção ativa** através da integração de sensores biomédicos, biofeedback vibrotátil e Estimulação Elétrica Neuromuscular (EMS) num colete ergonómico.

## Arquitetura e Simulação Eletrónica
A prototipagem e simulação do circuito eletrónico foram desenvolvidas integralmente na plataforma **Tinkercad**, garantindo a validação lógica dos limiares de deteção antes da transição para o hardware físico.

* **Microcontrolador:** Arduino UNO R4 WiFi (processamento central e conetividade).
* **Sensores Biomédicos:**
  * 1x IMU MPU-6050 (T2-T6) para medir inclinação e rotação do tronco.
  * 4x *Flex Sensors* (Spectra Symbol 4.5") distribuídos pelos ombros e zona lombar para deteção de assimetrias e hiperlordose.
    
* **Atuadores (Lógica de Duas Fases):**
  1. **Motor Vibratório (10mm):** Feedback de alerta imediato.
  2. **Sistema EMS (XFT-120C):** Ativação dos músculos paravertebrais (T10-L4) para correção ativa caso o utilizador não ajuste a postura após o tempo de tolerância. *(Nota: Na simulação em Tinkercad, a atuação EMS foi validada visualmente através de sinalização LED)*.

## Informática Médica e Inteligência Artificial
O ecossistema digital do projeto estende a funcionalidade do colete para a palma da mão do utilizador e do fisioterapeuta:
* **Backend:** Desenvolvido em **Python 3.11** utilizando a framework **Flask** para a criação de APIs REST.
* **Inteligência Artificial:** Implementação de algoritmos de Machine Learning (`Scikit-learn`) para classificação automática de posturas, previsão de recaídas e geração de recomendações personalizadas.
* **Aplicação Móvel/Web:** Interfaces dedicadas para o Paciente (evolução diária, alertas) e para o Fisioterapeuta (painel clínico, ajuste de parâmetros à distância).

## Biomateriais e Design Têxtil
O colete foi desenhado para maximizar o conforto e a precisão das leituras:
* Fabricado em **Tecido Power Mesh** (nylon e elastano), proporcionando suporte, elasticidade e respirabilidade.
* Zonas de fixação em velcro com fios condutores integrados e conetores magnéticos, permitindo a fácil remoção do hardware para lavagem.
e`: Código fonte em C++ (máquina de estados, leitura de sensores).
* `/python_backend`: Servidor Flask e scripts de Machine Learning.
* `/tinkercad_simulation`: Esquemas do circuito e ficheiros exportados.
* `/docs`: Memória descritiva, relatórios clínicos e design têxtil.
