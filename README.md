# BDP-XFC: Una base de datos pública de la vida académica de la Facultad de Ciencias de la UNAM

## Introducción

Este trabajo surge de las necesidad de contar con datos sólidos para que distintos miembros de la comunidad de la Facultad de Ciencias puedan estudiar distintos problemas académicos y administrativos de la dependencia. Así mismo, se espera que dicha infromación ayude a proponer soluciones basadas en datos duros.

Las "Normas en materia de transparencia y acceso a la información" de la UNAM, en su Arículo 28, "Obligaciones de la Universidad", punto XVIII el deber de de transparentar "La información estadística o información cuantitativa, con la mayor desagregación posible, que genera la Universidad sobre el quehacer institucional en cumplimiento de sus facultades, funciones y competencias".

La Facultad de Ciencias ofrece parte de esta información mediante su sitio web. Sin embargo, no tiene un punto de acceso para consultas generales. El objetivo de este repositorio es crear y mantener una base de datos pública conformada por extracciones del sitio web oficial. En este trabajo se cuidan aspectos de información personal.

## La base de datos `BDP-XFC`

Nuestro trabajo comienza con el diseño de una base de datos y de su llenado a partir de extracción de la información pública del sistema XFC de la Facultad de Ciencias de la UNAM. A esta base de datos le llamamos `BDP-XFC`, como acrónimo de "base de datos pública tomada del proyecto XFC". La información se encuentra disponible en la carpeta `Data`.

En el documento [BDP-XFC-Definitividades.pdf](Papers/Definitividades/BDP-XFC-Definitividades.pdf) se explica más de las razones que llevaron a crear esta base de datos. Además, en el Apéndice 1 de dicho documento definimos la estructura formal de `BDP-XFC` como base de datos relacional. Ahí también se explican las seis tablas que la conforman y sus relaciones. Para cada campo se explica de dónde se obtuvo la información. En la mayoría de los casos, esto se hizo mediante un script en Python que explorara repetidamente la página de la Facultad de Ciencias. Se tomó la precaución de no comprometer datos personales. En la siguiente figura se resume la estructura:

![Estructura de BDP-XFC](/Figuras/DB-relations.png)

## Aplicaciones de `BDP-XFC`

### Indicadores para definitividades de profesores de asignatura de la Facultad de Ciencias de la UNAM

La idea inicial de crear esta base de datos surge de la necesidad concreta de estudiar problemas de pago, profesionalizacion de la docencia y estabilidad laboral de profesores de asignatura y ayudantes de la Facultad de Ciencias de la UNAM. Un estudio para este caso está disponible en el documento [BDP-XFC-Definitividades.pdf](Papers/Definitividades/BDP-XFC-Definitividades.pdf). Los archivos auxiliares para crear este documento se encuentran en la Jupyter Notebook `AnalisisAsignatura.ipynb`.

Una de las conclusiones del estudio es una confirmación cuantitativa de que la labor de docentes de asignatura ha aumentado en los últimos años.

![Grupos atendidos](/Figuras/GruposAtendidos.png)

También ha aumentado la cantidad de alumnos que atienden los profesores de asignatura. En la figura incluso se nota la deserción causada por la pandemia de COVID-19.

![Alumnos atendidos](/Figuras/AlumnosAtendidos.png)

Además de esto, en el documento se estudia para los últimos diez semestres cuántos grupos ha habido para cada materia. Por ejemplo, a continuación se muestra esto para Cálculo Diferencial e Integral I.

![Grupos de Cálculo I atendidos](/Figuras/GruposCalculoI.png)

También se estudia la distribución cantidad de veces que los profesores de asignatura han impartido cierta materia en los últimos 10 semestres. Por ejemplo, la siguiente figura dice que hay un profesor de asignatura que ha impartido Cálculo Diferencial e Integral siete veces, mientras que hay 2 que la han impartido 6 veces.

![Distribución de veces impartidas por materia](/Figuras/HistVecesCalc.png)

## Uso de la base de datos

La base de datos es de libre acceso. De hecho, la idea de hacerla pública es que se use exhaustivamente para reconocer, estudiar y resolver problemas de la comunidad de la Facultad de Ciencias de la UNAM. Si la usas para un documento escrito, por favor deja una cita con los siguientes datos:

Leonardo Martínez-Sandoval. "BDP-XFC: Una base de datos pública de vida académica de la Facultad de Ciencias de la UNAM". Web. (fecha de consulta). https://github.com/leomtz/BDP-XFC/
