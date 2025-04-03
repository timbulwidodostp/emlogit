# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# ECM algorithm for the multinomial logit model Use emlogit With (In) R Software
install.packages("remotes")
remotes::install_github("soichiroy/emlogit")
library("emlogit")
# Estimation ECM algorithm for the multinomial logit model Use emlogit With (In) R Software
emlogit_1 = read.csv("https://raw.githubusercontent.com/timbulwidodostp/emlogit/main/emlogit/emlogit_1.csv",sep = ";")
y <- emlogit_1 %>% select(choice)
Y <- model.matrix(~choice-1, data = y)
X <- emlogit_1 %>% select(college, hsg2, coml5) %>% data.matrix()
emlogit_1 <- emlogit(Y = Y, X = X)
summary(emlogit_1)
emlogit_2 = read.csv("https://raw.githubusercontent.com/timbulwidodostp/emlogit/main/emlogit/emlogit_2.csv",sep = ";")
Y <- emlogit_2 %>% select(LDP, NFP, SKG, JCP) %>% data.matrix()
X <- emlogit_2 %>% select(gender, education, age) %>% data.matrix()
emlogit_2 <- emlogit(Y = Y, X = X)
summary(emlogit_2)
# ECM algorithm for the multinomial logit model Use emlogit With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
