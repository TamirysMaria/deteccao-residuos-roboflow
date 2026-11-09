# helpdesk-facil
Documentação do projeto HelpDesk Fácil.
# Prática de Visão Computacional com Roboflow
## Detecção de Resíduos: Garrafas Plásticas e Latas

### 1. Objetivo da prática

O objetivo desta atividade foi desenvolver um modelo de visão computacional capaz de identificar e classificar resíduos descartados no ambiente, utilizando a plataforma Roboflow.

O projeto foi desenvolvido com foco na detecção de objetos em imagens, permitindo reconhecer garrafas plásticas e latas por meio de técnicas de aprendizado de máquina.

### 2. Criação do projeto

Inicialmente, foi criado um projeto na plataforma Roboflow com o nome **Litter Detection**, utilizando a tarefa de Object Detection (Detecção de Objetos).

Essa modalidade permite identificar objetos em imagens, indicando sua localização por meio de caixas delimitadoras (Bounding Boxes).

### 3. Organização do dataset

Foram utilizadas 28 imagens contendo diferentes tipos de resíduos descartados no ambiente.

O conjunto de dados foi organizado em duas classes:

- **Garrafas:** identificação de garrafas plásticas.
- **Latas:** identificação de latas de bebidas.

As imagens foram carregadas na plataforma e organizadas para a etapa de anotação.

### 4. Anotação das imagens

Na etapa de anotação, foram utilizadas caixas delimitadoras (Bounding Boxes) para marcar a localização dos objetos presentes nas imagens.

Cada objeto foi associado à sua respectiva classe, permitindo que o modelo aprendesse a diferenciar garrafas e latas.

Essa etapa é importante porque fornece exemplos identificados que serão utilizados durante o treinamento.

### 5. Criação da versão do dataset

Após a organização e anotação das imagens, foi criada a primeira versão do dataset (v1).

A divisão dos dados foi realizada da seguinte maneira:

| Conjunto | Quantidade | Percentual |
|---|---:|---:|
| Treinamento | 16 imagens | 57% |
| Validação | 6 imagens | 22% |
| Teste | 6 imagens | 21% |
| **Total** | **28 imagens** | **100%** |

Também foi configurado o pré-processamento das imagens, utilizando redimensionamento para 512 × 512 pixels.

A técnica de aumento de dados (Augmentation) foi mantida desativada na criação da versão.

### 6. Treinamento do modelo

Para o treinamento, foi selecionada a arquitetura **Roboflow RF-DETR (Small)**, destinada à tarefa de detecção de objetos.

Foram mantidas as configurações padrão de treinamento disponibilizadas pela plataforma, incluindo o pré-processamento e as configurações de hiperparâmetros.

O treinamento foi iniciado e concluído com sucesso, gerando um modelo capaz de realizar a identificação dos resíduos nas imagens.

### 7. Avaliação dos resultados

Após o treinamento, foram consultadas as métricas de desempenho apresentadas pelo Roboflow.

Os resultados obtidos foram:

| Métrica | Resultado |
|---|---:|
| mAP@50 | 81,1% |
| Precisão (Precision) | 87,5% |
| Recall | 80,0% |
| F1-Score | 83,3% |
| Latência | 56,4 ms |

As métricas permitem avaliar o desempenho do modelo:

- **mAP@50:** mede a qualidade geral das detecções considerando uma sobreposição mínima de 50% entre as caixas previstas e as reais.
- **Precisão:** indica a proporção de detecções realizadas corretamente entre todas as detecções feitas pelo modelo.
- **Recall:** representa a capacidade de identificar os objetos que realmente estão presentes nas imagens.
- **F1-Score:** combina precisão e recall em uma única medida.
- **Latência:** representa o tempo de resposta do modelo.

### 8. Testes do modelo

Na etapa de testes, foram utilizadas imagens do conjunto de teste para verificar se o modelo conseguia reconhecer corretamente os objetos.

A plataforma apresentou as imagens com as respectivas caixas delimitadoras, os nomes das classes identificadas e os níveis de confiança das previsões.

Em um dos exemplos observados, o modelo identificou uma garrafa com aproximadamente 91% de confiança.

Os testes permitiram verificar, na prática, a capacidade do modelo de reconhecer resíduos e diferenciar as classes cadastradas.

### 9. Resultado final

Após a realização das etapas, o modelo foi salvo e ficou disponível na seção **My Models** da plataforma Roboflow.

O modelo gerado recebeu o nome:

`litter-detection-v3cad-9rrkl-1-rfdetr-small-t1`

Não foi realizada a implantação (Deploy), pois o objetivo da atividade era desenvolver, treinar e demonstrar o funcionamento do modelo.

### 10. Conclusão

A prática permitiu conhecer e aplicar as principais etapas do desenvolvimento de um modelo de visão computacional utilizando a plataforma Roboflow.

Durante a atividade, foi possível criar um projeto, organizar um conjunto de imagens, realizar anotações, configurar um dataset, treinar um modelo e avaliar seus resultados por meio de métricas de desempenho.

Os resultados demonstraram que o modelo conseguiu identificar garrafas plásticas e latas nas imagens de teste, apresentando 81,1% de mAP@50 e 87,5% de precisão.

Conclui-se que a atividade contribuiu para compreender como a inteligência artificial e a visão computacional podem ser utilizadas para identificar e classificar resíduos, podendo auxiliar em futuras soluções voltadas à gestão e ao descarte adequado de materiais recicláveis.
