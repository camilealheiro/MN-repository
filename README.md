# Análise de Algoritmos para Classificação de Imagens de Micronúcleo

Neste repositório estão os códigos utilizados na realização dos testes com os modelos YOLO para a detecção das classes desejadas (BN, BNMN, MN). Além disso, também está a forma que foi conduzido o experimento de junção de modelos diferentes (ensemble), a fim de tentar otimizar os resultados da detecção, e o pós-processamento aplicado após a etapa de ensemble.   

## teste-3classes-yolo.ipynb
Neste notebook está o código utilizado para treinamento dos modelos YOLO, tanto o YOLOv11 quanto o YOLOv12.   
Também contém funções auxiliares que realizam a vizualização das bounding boxes preditas baseado no ground truth, podendo conter 4 tipos de informação visual:
- Verde: classe correta e IOU > 0.5
- Amarelo: classe correta e IOU < 0.5
- Azul: sem detecção (IOU = 0)
- Vermelho: detecção incorreta

<p align="center">
  <img width="30%" height="auto" alt="BNMN151" src="https://github.com/user-attachments/assets/72b2d833-1526-4512-875a-f8f9f7ea7528" />
  <img width="30%" height="auto" alt="BNMN187" src="https://github.com/user-attachments/assets/06157fb1-adc1-4c2e-b2b6-c9643c2b3b2e" />
  <img width="30%" height="auto" alt="BNMN185" src="https://github.com/user-attachments/assets/cea1f6db-376f-4be2-b8c2-2c283cb61ff4" />
</p>

Por fim, o notebook posui uma seção de remoção de classes dos labels do ground truth, para que possam ser treinados modelos com números de classes diferentes (2 classes - BN e BNMN e 1 classe - MN).


## 
