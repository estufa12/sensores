# sensores

Objetivo é desenvolver um codigo onde seja calculado:

Temperatura do Bulbo Seco //DHT

Umidade Relativa  //DHT

Ponto de Orvalho  //DHT


Pressão Barometrica (baseada na altitude)
      
        P1 = 1013.3 / EXP [Z /(8430.15 - Z * 0.09514)]
          Onde:
          P1 = Pressão em Hpa a altitude Z metros
          Z = altitude em metros





Temperatura do Bulbo Umido (calculada com base na temperatura e umidade relativa)

Umidade Absoluta

 
Pressão de Saturação por Vapor de água

         Pvs = 6,11 * exp [(17,27 * T) / (237,3 + T)]
          Onde:
          T = temperatura em Celsius
          Pvs = Pressão de Vapor de saturação em Hpa
      

Pressão de Vapor 

  1)    Pv = 6.112 * EXP [17.7 * Td / ( Td + 243.5)]
          onde:
          Pv = Pressão de Vapor em Hp
          Td = Temperatura do ponto de Orvalho
        
        e/ou
        
  2)    Pv = Pvs - 0.66*103 * P * (Ts - Tu) * (1 + 1.146 * 103 * Tu)
        
          Onde:
          Pvs = Pressão de Vapor de saturação em Hpa
          P = Pressão atmosferica
          Ts = Temperatura Bulbo Seco (DHT)
          Tu = Temperatura Bulbo Umido
