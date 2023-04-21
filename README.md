# MCDropout-Novo domínio- Tracao
Aplicação do método de MC Dropout para o caso de uma modelagem de ensaio de tração em concreto
Incerteza Epistêmica em Redes Neurais - Gerson Eduardo de Mello

Esta é uma aplicação do método de incerteza em redes neurais proposto por Yarin Gal. O Dataset escolhido simulado aleatoriamente de um ensai ode tração onde a função é perfeitamente conhecida, ou seja T=4*F/(D².pi). Assim espera-se um resultado muito satisfatório uma vez que foram criados 1000 resultados deste ensaio vaiando F de 100 a 400 N e vartiando D de 50 a 150 mm. Foram usados 70% no treino e 30% no teste.

#Descrição do método proposto por Yarin Gal:

Em 2015, Yarin Gal mostrou que é possível obter incerteza a partir de redes neurais quase que gratuitamente, se olhássemos técnicas de regularização estocásticas, como Dropout, sob uma perspectiva Bayesiana. Dropout (Srivastava et al, ‎2014) é uma técnica utilizada na maioria das redes neurais modernas para prevenir sobre-ajustamento. Durante o treinamento, Dropout funciona zerando aleatoriamente uma percentagens de neurônios nas camadas da rede neural. No momento de fazer previsões, todos os neurônios são mantidos e a rede neural atua como uma grande mistura de sub-redes menores. Durante o treinamento do modelo, nada muda; mas, durante o teste mantemos a probabilidade de Dropout fixada durante o treino e realizamos T forward-pass pela rede, coletando assim T previsões y para cada amostra. Assim para cada ponto teremos uma previsão para a média e uma previsão para a variância, que será nossa medida de incerteza.
