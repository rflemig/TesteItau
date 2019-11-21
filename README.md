# TesteItau

## Acesso a API do twitter
BiBlioteca twitter

import tweepy as tw

consumer_key = ''
consumer_secret = ''
access_token = ''
access_token_secret = ''


## AUTENTICAÇÃO 
auth = tw.OAuthHandler(consumer_key, consumer_secret)

auth.set_access_token(access_token,access_token_secret)

api = tw.API(auth)

tweet = api.update_status("openapis")

# VALIDAÇÃO DO CONTEUDO COLETADO
tweet._json

# PESQUISANDO TWITTER

tweets = tw.Cursor(api.search,
          q="openapis",
          since='2019-01-01').items(10)
          
 for tweet in tweets:
  print(tweet.text)
  
  
  
  apis = ['openbanking','apifirst','devops','cloudfirst','microservices','apigateway','oauth','swagger','raml','openapi']
  
  # CONTAR QUANTAS INFORMAÇÕES EXISTEM
  
  len(apis)
  
  
  tweets = tw.Cursor(api.search,
          q="apifirst",
          since='2019-01-01').items(10)
          
          
  for tweet in tweets:
  print(tweet.text)
  
  

