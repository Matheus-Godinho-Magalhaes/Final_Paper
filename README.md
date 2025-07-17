# 🦯 Ferramenta Assistiva com Inteligência Artificial para Locomoção no Campus da UFMG

Este repositório contém o código-fonte, arquivos de configuração e documentação do Trabalho de Conclusão de Curso (TCC) intitulado **"Desenvolvimento de uma Ferramenta com Inteligência Artificial para Assistência à Locomoção de Pessoas com Deficiência Visual no Campus da UFMG"**, realizado como parte do curso de Engenharia Mecânica na Universidade Federal de Minas Gerais (UFMG).

---

## 🎯 Objetivo

Desenvolver uma solução baseada em **visão computacional** para detecção de objetos de interesse (bancos, faixas de pedestre, placas de ônibus) com o objetivo de auxiliar a **locomoção de pessoas com deficiência visual** em ambientes universitários, por meio de alertas sonoros e interpretação de cena em tempo real.

---

## 💡 Motivação

Pessoas com deficiência visual enfrentam barreiras significativas em sua mobilidade cotidiana, especialmente em ambientes complexos como o campus universitário. A proposta visa unir **inteligência artificial**, **visão computacional** e **acessibilidade digital** para promover inclusão e autonomia.

---

## ⚙️ Funcionalidades

- Detecção em tempo real de:
  - 🪑 Bancos
  - 🛑 Faixas de pedestre
  - 🚌 Placas de ponto de ônibus
- Feedback sonoro com base na classe e posição do objeto
- Treinamento com dataset personalizado capturado no campus Pampulha/UFMG
- Arquitetura baseada no modelo YOLOv11 com refinamento fino (fine-tuning)

---

## 🧠 Tecnologias Utilizadas

- Python 3.10
- YOLOv11 (Ultralytics)
- OpenCV
- Google Colab (para treinamento)
- PyTorch
- Roboflow (anotação e manipulação do dataset)
- CUDA (GPU - Google Colab Tesla T4)

---

## 📦 Dataset

O dataset foi capturado diretamente no campus da UFMG, contendo imagens em diferentes horários do dia (ambiente diurno e noturno), e anotado com três classes principais:

- **banco**
- **faixa_pedestre**
- **placa_onibus**

Total aproximado: 1444 imagens com data augmentation

**Observação:** Por questões de privacidade e ética, o dataset completo não está disponível publicamente neste repositório. Caso tenha interesse, entre em contato.

---

## 📊 Resultados
- mAP@0.5: 0.967
- Precision média: 0.927
- Recall médio: 0.936
- Inferência em tempo real (~23 ms por imagem)
- Análises qualitativas indicam boa performance em ambiente diurno e desempenho aceitável em ambiente noturno com baixa iluminação.

## ⚠️ Limitações
- Redução de desempenho notável em ambientes com baixa iluminação
- Alguns falsos positivos em objetos visualmente ambíguos
- Não testado ainda com usuários reais

## 📌 Trabalhos Futuros
- Inclusão de sensores complementares (ex: LIDAR ou IR)
- Validação com usuários com deficiência visual
- Expansão do dataset noturno
- Interface sonora mais adaptável