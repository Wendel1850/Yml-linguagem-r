# Carregar um conjunto de dados
data(mtcars)

# Visualizar os primeiros registros do conjunto de dados
head(mtcars)

# Calcular a média de uma variável
mean(mtcars$mpg)

# Calcular a correlação entre duas variáveis
cor(mtcars$mpg, mtcars$wt)
# Carregar a biblioteca ggplot2
library(ggplot2)

# Criar um gráfico de dispersão
ggplot(mtcars, aes(x = wt, y = mpg)) + 
  geom_point()

# Criar um gráfico de barras
ggplot(mtcars, aes(x = factor(cyl))) + 
  geom_bar()
  # Criar um modelo linear
modelo <- lm(mpg ~ wt, data = mtcars)

# Visualizar os resultados do modelo
summary(modelo)

# Prever valores com o modelo
previsao <- predict(modelo, newdata = data.frame(wt = 3))
# Carregar a biblioteca caret
library(caret)

# Criar um modelo de classificação
modelo <- train(mpg ~ ., data = mtcars, method = "lm")

# Prever valores com o modelo
previsao <- predict(modelo, newdata = mtcars)
# Carregar a biblioteca caret
library(caret)

# Criar um modelo de classificação
modelo <- train(mpg ~ ., data = mtcars, method = "lm")

# Prever valores com o modelo
previsao <- predict(modelo, newdata = mtcars)
