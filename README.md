# Tarea2_FOR_LOOP
hermosa tarea para el hermoso ramo de big data


#############Los bases se enumeran a continuación:#############

#1.pequena_peru.csv
#2.micro_peru.csv
#3.medianas_peru.csv
#4.grandes_peru.csv
#5.pequena_colombia.csv
#6.micro_colombia.csv
#7.medianas_colombia.csv
#8.grandes_colombia.csv
#9.pequena_chile.csv
#10.micro_chile.csv
#11.medianas_chile.csv
#12.grandes_chile.csv

#############Los atributos de las bases son:#############

#Fecha:indica el periodo.
#Pais: País de origen de las empresas.
#Ingresos: ingresos de explotación de las empresas.
#Costos: costos de explotación de las empresas.
#procentaje_muejeres: participación de mujeres que trabajan en la empresa.
#exportaciones: monto en millones de dólares de cuanto exportan estas empresas.
#importaciones: monto en millones de dólares de cuanto importan estas empresas. 
#endeudamiento: ratio de deuda financiera sobre activos totals.
#morosidad: tasa de castigo por morosidad.
#reservas: activos que mantienen sin movimiento en caso de dificultades.
#spread: tasa de premio por endeudarse.
#tasa_interes: tasa de interés a la que pueden endeudarse.


#############Se le pide lo siguiente:#############


#1) Cargue las bases de datos incoporando en cada una de ellas la variable “tamanio”,
#donde indique de que tamaño es la empresa de ese país.(1 pto)
#2) Reuna todas las bases en una sola y 
#defina de qué tipología (tipo de datos) son cada una de las variables que se encuentran en la data.(1 pto)
#3) Determine a través del uso de condicionales y/o for cuántas obervaciones tiene Peru versus Chile.(2 pto)
#4) Determine a través del uso de condicionales y/o for 
#¿cuál es el país con mayor ingresos de explotación para los años que considera la muestra.(2 pto)
#5) Genere una variable(columna) , donde si el país es Chile multiplique la tasa de interes por 0,1, 
#cuando sea Peru le sume 0,3 y, y finalmente si es Colombia divida por 10 (2 ptos).Use condicionales y/o for.
#6) Reemplace en la columna exportaciones con 1 cuando es mayor a 2,1, con un 2 cuando es menor 2,1y un 3 cuando es igual a 2,1, 
#redondee al primer decimal la variable(2 ptos). Use condicionales y/o for.



#BONUS TRACK
#Este ejercicio es opcional y le entregará 5 décimas a su nota final
#7) Gráfique algunas variables seleccionadas, las cuales puedan responder a una pregunta que se haga con respecto a los datos.


###############NUMERO_1###############

library(readr)
grandes_chile <- read_delim("tarea 2/grandes_chile.csv", 
                            ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("grandes"), size = 65, replace = TRUE)

grandes_chile<-data.frame(grandes_chile,tamano)

View(grandes_chile)
print(grandes_chile)

library(readr)
grandes_colombia <- read_delim("tarea 2/grandes_colombia.csv", 
                               ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("grandes"), size = 65, replace = TRUE)

grandes_colombia<-data.frame(grandes_colombia,tamano)

View(grandes_colombia)
print(grandes_colombia)

library(readr)
grandes_peru <- read_delim("tarea 2/grandes_peru.csv", 
                           ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("grandes"), size = 65, replace = TRUE)

grandes_peru<-data.frame(grandes_peru,tamano)

View(grandes_peru)
print(grandes_peru)


library(readr)
medianas_chile <- read_delim("tarea 2/medianas_chile.csv", 
                             ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("medianas"), size = 65, replace = TRUE)

medianas_chile<-data.frame(medianas_chile,tamano)

View(medianas_chile)
print(medianas_chile)

library(readr)
medianas_colombia <- read_delim("tarea 2/medianas_colombia.csv", 
                                ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("medianas"), size = 65, replace = TRUE)

medianas_colombia<-data.frame(medianas_colombia,tamano)

View(medianas_colombia)
print(medianas_colombia)

library(readr)
medianas_peru <- read_delim("tarea 2/medianas_peru.csv", 
                            ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("medianas"), size = 65, replace = TRUE)

medianas_peru<-data.frame(medianas_peru,tamano)

View(medianas_peru)
print(medianas_peru)

library(readr)
micro_chile <- read_delim("tarea 2/micro_chile.csv", 
                          ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("micro"), size = 65, replace = TRUE)

micro_chile<-data.frame(micro_chile,tamano)

View(micro_chile)
print(micro_chile)

library(readr)
micro_colombia <- read_delim("tarea 2/micro_colombia.csv", 
                             ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("micro"), size = 65, replace = TRUE)

micro_colombia<-data.frame(micro_colombia,tamano)

View(micro_colombia)
print(micro_colombia)

library(readr)
micro_peru <- read_delim("tarea 2/micro_peru.csv", 
                         ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("micro"), size = 65, replace = TRUE)

micro_peru<-data.frame(micro_peru,tamano)

View(micro_peru)
print(micro_peru)

library(readr)
pequena_chile <- read_delim("tarea 2/pequena_chile.csv", 
                            ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("pequena"), size = 65, replace = TRUE)

pequena_chile<-data.frame(pequena_chile,tamano)

View(pequena_chile)
print(pequena_chile)

library(readr)
pequena_colombia <- read_delim("tarea 2/pequena_colombia.csv", 
                               ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("pequena"), size = 65, replace = TRUE)

pequena_colombia<-data.frame(pequena_colombia,tamano)

View(pequena_colombia)
print(pequena_colombia)

library(readr)
pequena_peru <- read_delim("tarea 2/pequena_peru.csv", 
                           ";", escape_double = FALSE, trim_ws = TRUE)
tamano<-sample(c("pequena"), size = 65, replace = TRUE)

pequena_peru<-data.frame(pequena_peru,tamano)

View(pequena_peru)
print(pequena_peru)



###############NUMERO_2###############

names(grandes_chile)
names(grandes_peru)
names(grandes_colombia)
names(medianas_chile)
names(medianas_colombia)
names(medianas_peru)
names(micro_chile)
names(micro_colombia)
names(micro_peru)
names(pequena_chile)
names(pequena_colombia)
names(pequena_peru)

SuperBaseDeDatosMamalona <- data.frame(grandes_chile,grandes_colombia,grandes_peru,medianas_chile,medianas_colombia,medianas_peru,micro_chile,micro_colombia,micro_peru,pequena_chile,pequena_colombia,pequena_peru)


#fecha             -> character
#pais              -> character
#tamano            -> character
#ingresos          -> double
#costos            -> double
#porcentaje_mujeres-> character
#exportaciones     -> double
#importaciones     -> double
#endeudamiento     -> character
#morosidad         -> character
#reservas          -> character
#spread            -> character
#tasa interes      -> character
#tamano            -> character

###############NUMERO_3###############






  


###############NUMERO_4###############
###############NUMERO_5###############
###############NUMERO_6###############


#6) Reemplace en la columna exportaciones con 1 cuando es mayor a 2,1, con un 2 cuando es menor 2,1y un 3 cuando es igual a 2,1, 
#redondee al primer decimal la variable(2 ptos). Use condicionales y/o for.




###############NUMERO_7###############




boxplot(tamano)



