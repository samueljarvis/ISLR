pacman::p_load(
  "tidyverse",
  "magrittr",
  "ISLR",
  "MASS"
)

lm.fit = lm(formula = medv ~ lstat, data = Boston)

lm.fit %>% names()


lm.fit %>% confint()

lm.fit %>% coef()

topred <- data.frame(lstat = c(5, 10, 15))

predict(lm.fit, topred, interval = "confidence")

predict(lm.fit, topred, interval = "prediction")

plot(Boston$lstat, Boston$medv)
abline(lm.fit)

par(mfrow = c(2, 2))
plot(lm.fit)

plot(predict(lm.fit), residuals(lm.fit))
plot(predict(lm.fit), rstudent(lm.fit))
