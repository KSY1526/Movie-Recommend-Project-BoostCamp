# Movie Recommendation

![image](https://user-images.githubusercontent.com/68258495/211189168-0228f7ae-6a05-4691-a59b-e2a2e6cc8155.png)
# π RECCAR νμ μκ°

| <img src="https://user-images.githubusercontent.com/79916736/207600031-b46e76d2-cba3-4c94-9fc3-d9f29cd3bef8.png" width=200> | <img src="https://user-images.githubusercontent.com/113089704/208005478-0501fcea-89e8-42cd-959a-226c3ddb5b63.jpg" width=200> | <img src="https://user-images.githubusercontent.com/79916736/207601023-bbf9e64f-1447-41d8-991f-677593094592.png" width=200> | <img src="https://user-images.githubusercontent.com/79916736/207600724-c140a102-39fc-4c03-8109-f214773a64fc.png" width=200> | <img src="https://user-images.githubusercontent.com/65999962/210237522-72198783-f40c-491b-b8a7-6e6badf6cc24.jpg" width=200> | <img src="https://user-images.githubusercontent.com/79916736/208005357-e98d106d-a207-4acd-ab4b-1abf7dbcb69f.png" width=200> |
| :-------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------: |
|                                           [κΉμ±μ°](https://github.com/KSY1526)                                            |                                           [λ°°μ±μ¬](https://github.com/SeongJaeBae)                                            |                                            [μμΉν](https://github.com/Seunghoon-Schini-Yang)                                            |                                         [μ‘°μμ°](https://github.com/Suyeonnie)                                          |                                            [νμ¬ν](https://github.com/secrett2633)                                            |                                            [ν©μ ν](https://github.com/HSUNEH)                                            |

<br />
<br />

# ποΈ νλ‘μ νΈ λͺ©ν
<!-- <p align="center"><img src="https://user-images.githubusercontent.com/65529313/168472960-0eac76e2-4fe3-4ebc-b093-f9c0aab59859.png" /></p> -->
- μ¬μ©μμ μν μμ²­ μ΄λ ₯ λ°μ΄ν°λ₯Ό λ°νμΌλ‘, μ¬μ©μκ° λ€μμ μμ²­ν  μν λ° μ’μν  μνλ₯Ό μΆμ²

<br />
<br />

# π» νμ© μ₯λΉ
- GPU Tesla V100-PCIE-32GB

<br />
<br />

# ππ»ββοΈπ»ββοΈ νλ‘μ νΈ ν κ΅¬μ± λ° μ­ν 
- **κΉμ±μ°** : EDA / μ λ°μ μΈ ν νλ‘μ νΈ νμλΌμΈ μ€μ  / Rule-based λͺ¨λΈ μ€κ³ / λ² μ΄μ€λΌμΈ μ£Όμ μΆκ° λ° κ°μ  μμ
- **λ°°μ±μ¬** : AutoEncoder λ° glocal-K λͺ¨λΈ μ μ©, EASE λͺ¨λΈ μ μ© λ° νλΌλ―Έν° νλ, λ² μ΄μ€λΌμΈ μ£Όμ μΆκ°
- **μμΉν** : EDA / λ² μ΄μ€λΌμΈ μ£Όμ μΆκ° λ° κ°μ  μμ / MF λͺ¨λΈ μ§μ  κ΅¬ν λ° μ μ©
- **μ‘°μμ°** : EASE λͺ¨λΈ μ μ© / lightFM λͺ¨λΈ μ μ© 
- **νμ¬ν** : AutoEncoder μ μ© / λ² μ΄μ€λΌμΈ μ£Όμ μΆκ° / λ―Έμ μ μΆ μ½λ μμ±
- **ν©μ ν** : λν λ―Έμ κ³Όμ  μ£Όμ μΆκ° / λ² μ΄μ€λΌμΈ μ£Όμ μΆκ°

<br />
<br />

# π¨βπ©βπ§βπ¦ νμ λ°©μ
#### a. Zoom (Google Meet)
#### b. Notion
#### c. Slack
#### d. Google Docs

<br />
<br />

# π’ νλ‘μ νΈ μν μ μ°¨

#### 1. EDA
#### 2. Rule-based Model
#### 3. SASRec Model (S3-Rec with no Pre-training)
#### 4. Hyperparameter Tuning (Wandb)
#### 5. Ensemble (SASRec + EASE)

<br />
<br />

# β¨οΈ Model Architecture
```
μμΈν μ§ν κ³Όμ μ λ°νμλ£ λ΄ PDF νμΌμ μ°Έκ³ ν΄μ£ΌμΈμ!
```
## Rule-Base λͺ¨λΈ
```
Model_ipynb/KSY_rulbase.ipynb μ€ν
```

## S3-Rec λͺ¨λΈ (Baseline)

μν μΆμ² λνλ₯Ό μν S3-Rec λ² μ΄μ€λΌμΈ μ½λμλλ€.<br>
λ€μ μ½λλ₯Ό λνμ λ§κ² μ¬κ΅¬μ± νμ΅λλ€.

- λΌλ¬Έ λ§ν¬: https://arxiv.org/abs/2008.07873
- μ½λ μΆμ²: https://github.com/aHuiWang/CIKM2020-S3Rec

### Installation

```
pip install -r requirements.txt
```

### How to run
0. Encoding
   ```
   ensamble.ipynbλ‘ μΈμ½λ© λ train_new νμΌ μμ±
   ```
1. Pretraining
   ```
   python run_pretrain.py
   ```
2. Fine Tuning (Main Training)
   1. with pretrained weight
      ```
      python run_train.py --using_pretrain
      ```
   2. without pretrained weight
      ```
      python run_train.py
      ```
3. Inference
   ```
   python inference.py
   ```
4. Decoding
   ```
   ensamble.ipynbλ‘ λμ½λ© λ submission.csv νμΌ μμ±
   ```
   
<br />

## EASE
```
EASE/bae_EASE.ipynb μ€ν
```

## Ensemble
```
ensemble.ipynb μ€ν
```

<br />
<br />

# π― νλ‘μ νΈ μν κ²°κ³Ό - μ΅μ’ Private 2λ±

- Private λ¦¬λλ³΄λ μ€μ½μ΄ Recall@10 κΈ°μ€μΌλ‘ μμ μ μ 

|λ¦¬λλ³΄λ| Recall@10  |     μμ     |
|:--------:|:------:|:----------:|
|public| 0.1869 |  **2μ**   |
|private| 0.1699 | **μ΅μ’ 2μ** |

![image](https://user-images.githubusercontent.com/68258495/211190290-e59bc060-2dc8-4660-a8ef-d03522c4c10b.png)






