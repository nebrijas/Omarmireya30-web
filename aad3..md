# AD3

Esta es la actividad dirigida 3 que consiste en hacer un ejercicio de programación literaria aprovechando el código que hemos usado en Programación con Python donde realizamos web scrapping. Segidamente muestro el código fuente


## Código fuente 

```
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
 
resultados = []
 
req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')
 
tags = soup.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')
 
tags = soup2.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')
 
tags = soup3.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')
 
tags = soup4.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')
 
tags = soup5.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')
 
tags = soup6.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')
 
tags = soup7.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')
 
tags = soup8.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')
 
tags = soup9.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')
 
tags = soup10.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')
 
tags = soup11.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')
 
tags = soup12.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')
 
tags = soup13.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')
 
tags = soup14.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')
 
tags = soup15.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')
 
tags = soup16.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')
 
tags = soup17.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
 
os.system("clear")
 
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))
 
print(colored("Igualdad", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))
 
print(colored("Mujeres", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))
 
print(colored("Mujer", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))
 
print(colored("Brecha salarial", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))
 
print(colored("Machismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))
 
print(colored("Violencia", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))
 
print(colored("Maltrato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))
 
print(colored("Homicidio", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))
 
print(colored("Género", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))
 
print(colored("Asesinato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))
 
print(colored("Sexo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

## Web Scrapping con Phyton

Pogramación literaria 

## Importamos las librerías

### Modulos del sistema

1. time:[Es un módulo que proporciona varias funciones relacionadas con el tiempo](https://docs.python.org/es/3/library/time.html)
2. csv: [Los valores separados por coma son el formato más común de importación y exportación de hojas de cálculo y bases de datos](https://docs.python.org/es/3/library/csv.html)
3. re: [Este módulo proporciona operaciones de coincidencia de expresiones regulares similares a las encontradas en Perl.](https://docs.python.org/es/3/library/re.html)
4. os: [Este módulo provee una manera versátil de usar funcionalidades dependientes del sistema operativo](https://docs.python.org/es/3.10/library/os.html)


## Importar Librerías 

Librerías 

Aquí voy a importar librerías

1. request:[Libreria de Phyton](https://pypi.org/project/requests/)
2. pandas: [Potentes estructuras de datos para análisis de datos, series temporales y estadísticas](https://pypi.org/project/pandas/)
3. bs4: [Beautiful Soup es una biblioteca que facilita extraer información de páginas web](https://pypi.org/project/beautifulsoup4/)
4. termecolor:[Lo que hace el módulo termcolor es que le permite imprimir texto en color en el shell.](https://replit.com/talk/learn/How-to-Use-Termcolor-In-Python/24684)

## Instalamos librerías 

Las librerías que vienen con Phyton no necesitan ser instaladas, pero las otras sí


```python
pip install requests bs4 pandas termcolor
```

    Requirement already satisfied: requests in c:\users\wow\anaconda3\lib\site-packages (2.27.1)Note: you may need to restart the kernel to use updated packages.
    
    Requirement already satisfied: bs4 in c:\users\wow\anaconda3\lib\site-packages (0.0.1)
    Requirement already satisfied: pandas in c:\users\wow\anaconda3\lib\site-packages (1.4.2)
    Requirement already satisfied: termcolor in c:\users\wow\anaconda3\lib\site-packages (1.1.0)
    Requirement already satisfied: charset-normalizer~=2.0.0 in c:\users\wow\anaconda3\lib\site-packages (from requests) (2.0.4)
    Requirement already satisfied: urllib3<1.27,>=1.21.1 in c:\users\wow\anaconda3\lib\site-packages (from requests) (1.26.9)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\wow\anaconda3\lib\site-packages (from requests) (2021.10.8)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\wow\anaconda3\lib\site-packages (from requests) (3.3)
    Requirement already satisfied: beautifulsoup4 in c:\users\wow\anaconda3\lib\site-packages (from bs4) (4.11.1)
    Requirement already satisfied: python-dateutil>=2.8.1 in c:\users\wow\anaconda3\lib\site-packages (from pandas) (2.8.2)
    Requirement already satisfied: pytz>=2020.1 in c:\users\wow\anaconda3\lib\site-packages (from pandas) (2021.3)
    Requirement already satisfied: numpy>=1.18.5 in c:\users\wow\anaconda3\lib\site-packages (from pandas) (1.21.5)
    Requirement already satisfied: six>=1.5 in c:\users\wow\anaconda3\lib\site-packages (from python-dateutil>=2.8.1->pandas) (1.16.0)
    Requirement already satisfied: soupsieve>1.2 in c:\users\wow\anaconda3\lib\site-packages (from beautifulsoup4->bs4) (2.3.1)
    

### Importamos las librerías

Empleamos tres módulos diferentes para importar libreria

1. Algunas librerías son importadas directamente. Como el caso de requests.
2. Otras, en cambio, se importan cambiándoles el nombre que se va a emplear para invocarlas. Este es el caso de pandas.
3. Por último, están las librerías de las que importamos determinados componentes. En este caso tenemos bs4 y termcolor.




```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
```

# Objetos Variables

Crearemos una serie de objetos o variables.


### Resultados

Creamos un objeto vacío denominado resultados para agregar los resultados del scrapping


```python
resultados =[]
```

Si pasamos la función type() podemos observar que este objeto es de tipo lista de Python. Este tipo de elemento es básico y fundamental para organizar información/datos.


```python
type(resultados)
```




    list



## Solicitud de acceso a datos en un sitio en línea

Se añade una variable con la que se hace uso de la solicitud req=requests.get("https://resultados.elpais.com") para recoger la información de esa URL.


```python
req = requests.get("https://resultados.elpais.com")
```

Si pasamos la función type() podemos observar que este objeto es de tipo Respuesta de modelo requests.


```python
type(req)
```




    requests.models.Response



Como está comentado en el propio código, se emplea un condicional if para que cuando el estatus no sea 200 el valor de vuelta no pueda leerse. Este valor 200 significa que la solicitud fue exitosa y el servidor respondió con los datos solicitados. En caso de que no se encuentre un resultado como el indicado se mostrará el mensaje No se puede hacer Web Scrapping en seguido de la URL errónea.


```python
# Si el estatus no es 200 no se puede leer la página
if (req.status_code != 200):
    raise Exception("No se puede hacer Web Scraping en"+ URL)
```

Si pasamos la función type() podemos observar que el objeto req.status_code es de tipo entero, por lo que el resultado será numérico.



```python
type(req.status_code)
```




    int



## BeautifulSoup

Se añade otra variable para aplicar Web Scrapping.



```python
soup = BeautifulSoup(req.text,'html.parser')
```

Si pasamos la función type() podemos observar que este objeto es de tipo bs4.


```python
type(soup)
```




    bs4.BeautifulSoup


También se añade la variable que sirve para encontrar todas las etiquetas <h2> dentro de la página anteriormente especificada.

```python
tags = soup.findAll("h2")
```

Si pasamos la función type() podemos observar que el objeto tags es de tipo Resultado del set de elementos bs4.


```python
type(tags)
```




    bs4.element.ResultSet



Se indica a través de un for, que se recorran todos los h2 dentro de la variable anterior y se imprima el texto dentro de la etiqueta. Posteriormente con resultados.append(h2.text) se añaden todos los textos dentro de las etiquetas a la lista inicial resultados.


```python
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

    El Tribunal Supremo deroga el derecho al aborto en Estados Unidos
    Las claves del aborto en EE UU tras la decisión del Supremo
    Biden pide al Congreso recuperar el derecho al aborto como ley federal
    Misuri y Texas, los primeros Estados que prohíben totalmente el aborto en Estados Unidos
    Video | Visita a una clínica en donde ya es delito practicar abortos
    El Supremo destruye un derecho fundamental de las mujeres
    La sentencia sobre el aborto cae como una maza en la clínica de Misisipi que ha perdido el caso
    Así se puede ver la alineación de cinco planetas, justo antes de cada amanecer
    El oro no es “del Rin”, sino del crimen
    Jesucristo armado en Brasil
    El mejor sexo de tu vida
    A medias
    18 migrantes muertos y 63 heridos en una avalancha al intentar entrar en España
    El apretón de manos de dos presidentes que se dan la espalda 
    El Gobierno de Colombia confirma tres casos de viruela del mono
    Cuba condena a cinco y nueve años de cárcel a los principales opositores del Movimiento San Isidro
    El FMI prevé un frenazo en la economía de Estados Unidos, pero cree que puede evitar la recesión
    Un hombre mata a tiros en un restaurante a su esposa, la cantante mexicana Yrma Lydya 
    Steven Spielberg: “John Williams va camino de ser eterno”
    La UE se prepara ante el riesgo de nuevos cortes de gas ruso
    El True Story Award premia a Jacobo García, reportero de EL PAÍS en México, por ‘Caribe turbio’
    La FINA prohíbe a Anita Álvarez, la nadadora que se desmayó, participar en la final por equipos en los Mundiales
    Anita Álvarez, la nadadora que se desmayó en el agua: “Sentí que todo se volvió negro. No recuerdo nada más”
    Así fue el rescate de la nadadora Anita Álvarez
    FOTOGALERÍA | El rescate, en imágenes
    El avispero de Los Altos de Chiapas: una bala en medio de los pulmones
    López Obrador asegura que México cumplirá con “todos los requisitos” para recuperar la categoría 1 en seguridad aérea
    
    
    Ucrania ordena la retirada de los militares del enclave estratégico de Severodonetsk 
    El Congreso aprueba la ley histórica que aumenta el control sobre las armas en EE UU
    La ONU concluye que la periodista de Al Jazeera Abu Akleh murió por disparos de fuerzas israelíes
    La paz global vive su peor momento de los últimos 15 años
    Nadie quiere el cuadro de Goya
    Sorolla y Esteban Vicente: convertir la pasión por los jardines en luz para su arte
    Julio Rojas, creador de la audioserie de ciencia ficción ‘Caso 63’: “Nos golpeó el futuro”
    ‘Aniquilación’, de Michel Houellebecq: confusión en el campo de batalla
    Escribir en soledad y a la vez conjuntamente  
    La casa de Ana Frank:  entre el comercio y la apropiación personal
    Denise Richards sigue los pasos de su hija y se crea una cuenta en OnlyFans
    ‘Podcast’ | Cuando tu intimidad se hace viral
    Mae West y la muerte de su fan número uno: una tragedia en el ocaso de la estrella más subversiva de Hollywood 
    Sharon Stone: “Perdí nueve hijos por abortos espontáneos. Las mujeres no tenemos un espacio donde discutir la profundidad de estas pérdidas”
    
    
    Christopher Mims: “Amazon sabe cómo para prevenir lesiones. Pero quizá dejaría de ganar dinero”
    Dentro o fuera de la metrópolis: ¿es posible un dinamismo artístico sin estar en las grandes ciudades?
    Repensar la función y el futuro del arte contemporáneo
    Gustavo Petro: la victoria final
    Ciudad Oculta: las drogas y el hambre no ceden en Argentina
    Bruno Pereira, un funcionario convertido en activista para proteger a los indígenas
    Así era América antes de que Colón la descubriera
    US Supreme Court overturns ‘Roe v Wade,’ ending federal abortion rights
    Trump tried to put a loyalist at the helm of the Justice Department to challenge Biden’s victory
    Anita Álvarez, the swimmer who fainted in the pool: ‘I felt everything turn black’
    WHO debates declaring monkeypox virus a global emergency
    Petro’s win in Colombia opens new era between Caracas and Bogotá
    Letras Americanas: la actualidad literaria de un continente vista por el escritor Emiliano Monge
    Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
    Toda la actualidad científica en el boletín de Materia
    Ideas: reportajes y entrevistas para entender el mundo
    Turquía desarticula una red iraní que planeaba atentar contra israelíes en Estambul
    Los talibanes, aislados y sin recursos, piden ayuda internacional para la emergencia del terremoto en Afganistán
    La candidatura de Ucrania espolea la impaciencia de los Balcanes para ingresar en la UE 
    Latinoamérica muestra su músculo ante el inicio del alza en las tasas de interés
    La inflación en México vuelve a escalar y se sitúa en 7,88% en junio
    Marilynn Malerba, la jefa de la tribu india Mohegan que firmará los nuevos billetes en Estados Unidos
    Por qué estamos cada vez más deprimidos
    La expansión de la viruela del mono empuja a la OMS a decidir si es una emergencia internacional
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    Así suena ‘Break My Soul’, lo nuevo de Beyoncé 
    Michael J. Fox, Diane Warren, Peter Weir y Euzhan Palcy recibirán los Oscar honoríficos
    María Pagés: “A los lugares cercanos se va a seguir yendo, pero a los lejanos… quién va a poder comprar los billetes”
    Se llama Lucas, pero yo ya le llamo Diazepam: así me ha sobrepasado que mi perro tenga ansiedad por separación
    Las incógnitas de la pastilla milagrosa contra un tipo de calvicie
    Hachas, niños y asesinatos bajo césped artificial: así es la necrópolis monumental más antigua de España 
    Anita Álvarez, la nadadora que se desmayó en el agua: “Sentí que todo se volvió negro. No recuerdo nada más”
    Wimbledon no permite escapatoria: duro trazado para Nadal y Alcaraz
    Ya casi no hay goles de falta directa, y la culpa no es de los lanzadores
    La trampa mortal del trasvase Tajo-Segura: así se ahogan corzos y jabalíes en el canal 
    Dos veranos sin playa, cerrada por contaminación: “Si esto fuera Barcelona, se arreglaba en dos días”
    Vivir frente a un “vertedero” en el centro de Madrid: estruendo, hedor y ratas en Tirso de Molina
    Christopher Mims: “Amazon sabe cómo bajar el ritmo de trabajo para prevenir lesiones. Pero quizá dejaría de ganar dinero” 
    ¿Sigue siendo imprescindible tener un antivirus? 
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    El rechazo del PP complica la reforma exprés del PSOE para renovar el Constitucional
    El contrato del que cobró el hermano de Ayuso sigue bajo la lupa de la Fiscalía europea 
    Moreno anticipa “tiempos complicados” y dice que no tiene “varitas mágicas”
    ‘La clave’ de Balbín, gloria y caída del programa que cambió la televisión española
    ‘Maria Ressa, la periodista filipina “no exenta de ser asesinada”, por Ricardo de Querol
    Pepón Nieto denuncia que TVE vetó una de sus películas en ‘Cine de barrio’ y la corporación recula: se emitirá este sábado
    Los problemas crecen para los Bieber: Hailey, demandada por la marca de cosmética que lanzó hace una semana
    Guillermo de Inglaterra cumple 40 años como el candidato ideal para seguir la estela de Isabel II
    Los 40 años de Guillermo de Inglaterra en 16 fotos
    Volver a la escuela tras dos años de pandemia
    La discriminación contra las minorías sexuales limita el desarrollo de Latinoamérica
    Así fue nuestra experiencia de escribirnos con GPT-3, una máquina de inteligencia artificial
    Ir a un concierto o pintar nos repara emocionalmente
    Guy Standing: “Hemos dejado que la derecha se apropie de la libertad”
    Así era América antes de que Colón la descubriera
    Ya no se viaja igual que antes de la pandemia: estas son las nuevas modas del turismo 
    El salto mortal de Estrella Galicia 
    LaMDA, Google y cuando jugar con una inteligencia artificial es posible
    En los sesenta, todo se vendía con fotos
    La paz global vive su peor momento de los últimos 15 años
    Las crisis de hoy son diferentes
    En Flandes las bicis son para el verano: cuatro etapas en la región belga para el placer de viajar lento
    Las reseñas de los turistas, tan útiles o tan inútiles: una cuenta de Twitter señala comentarios absurdos sobre Asturias
    Brooke Shields: “Fue duro querer a mi madre alcohólica porque me sentía responsable de ella”
    Aura García-Junco, sobre las relaciones abiertas: “Quería entender por qué generan tanto rechazo”
    Eugenia Silva: “No he vivido situaciones extremas. Sabía qué quería y hasta dónde llegar”
    Las frustraciones de Wes Craven, el genio del terror que quería dirigir melodramas
    Refresco, fruta y salsa: tres fermentados caseros para principiantes
    Once buenos restaurantes tailandeses, vietnamitas e indonesios en España
    Las rentas más bajas soportan una presión fiscal similar a la del 1% más rico
    Fernando Tejero revela cómo Dani Martín le sacó de una pensión decadente tras llegar a Madrid para llevarle a vivir a casa de sus padres
    Ponte a prueba con nuestros crucigramas, sopas de letras, sudokus y juegos arcade
    Un exconcursante de ‘Operación Triunfo’ se lleva 9.000 ‘me gusta’ con su dura réplica a Ayuso
    El Bayern prepara un golpe al Barça
    Hidrógeno verde, la coincidencia más feliz de Mallorca
    


```python
type(resultados.append)
```




    builtin_function_or_method



Repetimos el proceso para las URLs de las subsecciones de https://elpais.com: internacional, opinión, España, economía, sociedad, educación, clima y medio ambiente, ciencia, cultura, babelia, deportes, tecnología, gente, televisión y eps. Para ello, se realiza el proceso previo de forma similar y se modifican los nombres de las variables poniéndosele números, por ejemplo, req2 para la URL https://elpais.com/internacional, y así sucesivamente.


```python
req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

    Fútbol: derechos equiparados
    El problema israelí se llama Netanyahu
    Un día muy triste para todas las mujeres
    Un Derby de platino
    Vidas gitanas
    Nostalgia de lo que abandonamos en Argelia
    Ucrania en la UE, fuerza mayor
    Hacia un nuevo modelo de residencias
    La tentación del exceso
    Luz y tinieblas
    El mejor sexo de tu vida
    A medias
    El clima incendiado
    El Roto
    Peridis
    Flavita Banana
    Riki Blanco
    Sciammarella
    Planeta de Plástico, por Malagón
    Envía tu carta
    Desmantelando la sanidad, que es gerundio
    La proyección de las elecciones en Andalucía
    Siempre pierden los mismos: los agricultores
    Opinar sin insultar
    Contra el conflicto de intereses, transparencia
    Entre los derechos de Esther López y los de los lectores
    El defensor del lector contesta
    El rechazo del PP complica la reforma exprés del PSOE para renovar el Constitucional
    Los independentistas piden al Congreso que denuncie al exministro Fernández Díaz por mentir a la Cámara
    18 migrantes muertos y 63 heridos en una avalancha al intentar entrar en Melilla
    La búsqueda de seguridad vence al cabreo
    Los errores se pagan
    Desborde popular en Andalucía
    Demasiado ruido en el Gobierno de coalición
    La ‘confederalización’ del PP
    Sánchez adelanta que las medidas anticrisis se prolongarán hasta final de año
    El contrato del que cobró el hermano de Ayuso sigue bajo la lupa de la Fiscalía europea 
    Castilla y León promete 35 millones para la sierra de la Culebra, más de la mitad del presupuesto antiincendios
    Porcuna, el feudo andaluz de Ciudadanos que marca el camino para atajar la crisis del partido
    El Gobierno impulsa una reforma legal para renovar el Constitucional
    Vídeo | Las imágenes de los inmigrantes detenidos por Marruecos en Nador
    Moreno avanza “tiempos complicados” y dice que no tiene “varitas mágicas”
    Una nueva suspensión de la moción de censura enquista la política local de Linares
    Aborto, ‘ley Celaá’, eutanasia: las sentencias más importantes a la espera de la renovación del Tribunal Constitucional
    Así giró Andalucía: la derecha lleva años creciendo sobre todo en barrios pobres
    El Ejecutivo lleva aprobados más de 10.000 millones en medidas en lo que va de año
    Un paraíso en el que avistar más de 20 especies de cetáceos
    El secreto de Fuerteventura se hace viral: la ‘playa de las palomitas’
    Artesanía y cultura que conquista a las ‘influencers’
    Más allá de la capital. El triunfo de la vida rural madrileña
    Así lucha la tierra del cerezo para conseguir un nuevo florecimiento económico
    “Siempre me ha parecido que los que iban disfrazados eran los demás”
    “La herramienta más poderosa para salvar a la humanidad son las matemáticas”
    El INE rebaja el crecimiento del primer trimestre en una décima, hasta el 0,2%, y confirma el enfriamiento de la economía
    España recibirá 7.800 millones más de lo previsto en ayudas directas del fondo europeo de recuperación
    Bruselas avala el rescate a Celsa y lo deja a expensas del acuerdo con los acreedores
    El Banco de España eleva a 23.000 millones los préstamos del ICO en peligro de impago
    Invierno crudo
    Aterrizaje suave sin fragmentación
    El ajuste fiscal que viene: ¿Qué opinan los ciudadanos?
    Las finanzas que corroen la industria 
    Una oportunidad perdida en el proceso de las energías renovables 
    La petrolera estatal de Argelia reclama a Técnicas Reunidas 80 millones de euros en plena crisis diplomática
    Ryanair no cancela ningún vuelo desde España en el primer día de huelga
    Indra se desploma en Bolsa casi un 15% tras el vuelco en su consejo 
    La SEPI rechaza el rescate de Ezentis y la acerca a la quiebra
    Room Mate pide el concurso de acreedores para dar entrada a un nuevo inversor
    El Gobierno retrasa el recargo a los combustibles para abaratar la luz y el recorte a las eléctricas por el CO₂
    La CNMC controla los márgenes de las gasolineras en tiempo real tras la bonificación de 20 céntimos
    La guerra entre los señores del acero se recrudece
    DAZN recupera el 80% de lo que pagó por el fútbol, pero tendrá difícil rentabilizarlo
    Los trabajadores de consultoras y tecnológicas secundan el primer paro de su historia: “No puede ser que la explotación sea norma” 
    La Reserva Federal ve a la banca de Estados Unidos preparada para hacer frente a una recesión
    Ferrari corre hacia un mundo más verde y caro
    Vientres de alquiler: una boyante y turbia industria que aprovecha las rendijas legales para enriquecerse
    Ya no se viaja igual que antes de la pandemia: estas son las nuevas modas del turismo 
    El salto mortal de Estrella Galicia 
    La guerra entre los señores del acero se recrudece
    Las rentas más bajas soportan una presión fiscal similar a la del 1% más rico
    La CNMV quiere que los inversores institucionales se impliquen a largo plazo en las cotizadas
    Las hipotecas a tipo fijo superan el 75% en abril y marcan un nuevo récord en plena escalada del euríbor
    Por qué el bitcóin ha caído un 70% desde máximos y por qué puede seguir a la baja
    Líos en la piscina comunitaria: normas y sentencias para un chapuzón seguro
    Parir en casa, educarlo por mi cuenta… ¿Qué puedo decidir sobre mi hijo y qué no?
    Saltarse un paso a nivel de camino a la oficina es accidente laboral
    Francisco Javier Blasco: “Llevamos años sin mejorar la eficacia de las políticas activas de empleo”
    ¿Es esta la edad dorada del emprendimiento universitario?
    Y después de la EBAU, ¿qué?
    Cancerberos del bienestar de la empresa
    Salud a golpe de clic con la cercanía del médico de cabecera
    Cómo garantizar la seguridad en un mundo de amenazas híbridas
    ¿Cuáles son los dilemas éticos del uso de la inteligencia artificial?
    Las aventuras de un par de calcetines que dan empleo a todo un pueblo
    Cultura financiera como punto de partida para volver a empezar
    Por qué digitalizar una pyme aporta más empleo
    Logística a bajas temperaturas, la revolución que vino del frío
    ‘Coopetir’: la actitud DFactory
    Así serán las ciudades de la (nueva) última milla
    PERTE Agroalimentario: ¿cómo acceder a los fondos europeos?
    Claves para internacionalizar mi negocio
    ¿Crisis de deuda mundial a la vista?
    ¿Está al frente España de la revolución del hidrógeno? 
    El momento de la energía solar
    Las principales reformas (con subvención europea) para ahorrar energía en la vivienda
    Gloria Ramos, cuando el afán de superación acaba en la alfombra roja 
    La importancia de la cultura financiera para tener una buena jubilación
    Hotmart y su plataforma 360 para creadores de contenidos
    Una aplicación para presentar la declaración desde casa y conseguir los máximos beneficios
    El Tribunal Supremo deroga el derecho al aborto en Estados Unidos
    El aborto en EE UU tras la decisión del Supremo: las claves
    Un día muy triste para todas las mujeres
    Un día muy triste para todas las mujeres
    El Supremo de Estados Unidos destruye un derecho fundamental de las mujeres
    El intento de suicidio de Juan y las somatizaciones de Carmen: ¿por qué los colegios necesitan un psicólogo educativo?
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    El origen de la hepatitis aguda infantil es todavía un misterio después de 894 casos, decenas de trasplantes y 18 muertes
    La Iglesia insiste en que no abrirá sus archivos al Defensor, aunque cederá datos de casos concretos que le solicite
    El nuevo sistema para evaluar los conocimientos digitales de los profesores valdrá en toda España
    El repunte de contagios de covid acelera los ingresos hospitalarios impulsado por nuevas variantes de la ómicron 
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    Un año de eutanasia en España: 172 casos y una gran desigualdad entre las comunidades autónomas
    La expansión de la viruela del mono empuja a la OMS a decidir si es una emergencia internacional
    El conde de Atarés asesinó a su mujer el día en que se disponía a abandonarle
    Sanidad descarta que la infección de la finca de Toledo sea un caso de cólera, aunque esté causada por la misma bacteria
    Las autoridades sanitarias del Reino Unido detectan el virus de la polio en las aguas residuales de Londres
    Seis de cada diez ciudadanos viven en comunidades autónomas con servicios sociales debilitados
    Mitos, falsedades, bulos y realidades sobre el VIH 40 años después
    Educadores con VIH para minimizar el impacto tras el primer diagnóstico
    El tremendo peso de la obesidad en España
    Interactivo | Los 14 cambios en los aeropuertos españoles que no ves y que ya están ocurriendo
    Encontrar empleo pese a los obstáculos. Por dónde empezar la búsqueda
    La fórmula de Carboneros para evitar el éxodo rural: trabajar cuidando a los vecinos 
    Consejos y cuidados para el primer verano con un gatito o un perrito
    ¿Qué tienen en común perros y gatos cuando son cachorros?
    La guía definitiva para alimentarnos mejor (y cuidar nuestra salud y la del planeta)
    Más vida después del cáncer de próstata avanzado 
    Cáncer de ovario, el más rebelde de los tumores ginecológicos
    El metro como refugio. De los andenes de Madrid en 1936 a los de Kiev en 2022
    La salud mental de los refugiados: cómo abrirse para cerrar las heridas
    El desconocido (y esencial) apoyo de los farmacéuticos a los pacientes crónicos
    El esfuerzo de una paciente por convertirse en su doctora
    Así es la vida de los refugiados ucranianos en España
    ¿Cómo será el envase para alimentos y bebidas del futuro?
    El intento de suicidio de Juan y las somatizaciones de Carmen: ¿por qué los colegios necesitan un psicólogo educativo?
    El nuevo sistema para evaluar los conocimientos digitales de los profesores valdrá en toda España
    Un aula de Vallecas se rebela contra los libros de texto que silencian a las mujeres
    Solo un 3% de alumnos de Cataluña pidió hacer el examen de Selectividad en castellano
    Subirats reinterpreta la ley de Universidades: freno a la precariedad, facilidades para los alumnos extranjeros y ciencia abierta
    “Los profesores no van a cambiar de golpe su forma de trabajar el curso que viene por la nueva ley educativa”
    Trampantojo de pescado y lasaña vegetal en el comedor: cientos de colegios buscan fórmulas para que llevar la alimentación responsable a los niños
    Vídeo | Las recetas del cocinero escolar para que los niños de El Grau coman sano y rico 
    Así puede convertirse un colegio en un espacio más fresco sin usar aire acondicionado
    209.691 candidatos compiten por una plaza en la última convocatoria sin ventaja aplastante para los interinos
    El mileurismo asoma en la mitificada carrera de dentista: “Nunca imaginé una situación así”
    Sin currículos
    La escuela concertada ante las desigualdades: el debate pendiente
    La equidad frente a las políticas educativas de privatización en Andalucía
    No hay lunes al sol en la Universidad
    Ofrecer comedor gratis en todos los colegios públicos es “alcanzable y urgente”: costaría 1.664 millones al año, según la ONG Educo  
    Una fórmula para que la escuela pública compita mejor con la concertada
    La pérdida de alumnos por el descenso de la natalidad está afectando con más fuerza a la escuela pública que a la concertada
    El Ayuntamiento de Madrid guarda en un cajón una herramienta ya pagada para ver los datos de contaminación al detalle 
    La implantación del nuevo Bachillerato general fracasa pese a su demanda potencial: “Creímos que lo pedirían seis alumnos y lo han hecho 27”
    Toni Solano, director de instituto: “Veo mal a los niños, necesitan muchísima ayuda”
    Niños, Administraciones y redes sociales: prohibir su uso con una mano y enseñar a crear contenidos con la otra
    El Gobierno aprueba el decreto de bachillerato: los alumnos podrán terminar con un suspenso y desembocará en una nueva Selectividad
    La ley del silencio dentro y fuera del aula
    Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
    Golpe a la temporalidad en las universidades: 25.000 profesores asociados serán indefinidos a tiempo parcial
    Antonio Abril: “Yo le decía a Castells: ‘Tienes que aguantar la presión, tienes que hacer la reforma universitaria”
    Los universitarios extranjeros podrán quedarse un año en España automáticamente al terminar la carrera
    Sierra de la Culebra: un incendio gigantesco que no pone en peligro a los lobos, pero sí un modelo de convivencia ejemplar
    La indignación crece sobre las ascuas del incendio en la sierra de la Culebra
    Jardines en los tejados, árboles africanos y calles pintadas de blanco: cómo adaptar la ciudad al calor extremo
    La construcción de 52 viviendas en una playa de Begur desata la indignación de las redes
    Un continente mortal para los defensores de la tierra
    Drama en la sierra de la Culebra, el paraíso del lobo ibérico que quedó abrasado por un rayo
    Alemania anuncia que recurrirá al carbón ante el recorte de suministro de gas ruso
    La inacción frente al cambio climático hará que sea habitual superar los 40 grados en junio en España
    Ibrahim Thiaw: “Hay que prepararse mejor frente a las sequías, los agricultores franceses están cultivando ya cereales africanos”
    La ola de calor provoca la caída de cientos de crías de vencejo en las calles de Sevilla y Córdoba
    “En Singapur ya se vende carne cultivada para alimentación” 
    La lección del martín pescador para afrontar la crisis ecológica
    Estocolmo+50: mirar atrás para tomar impulso
    El verano ya no es lo que era 
    Juan Serna, Premio Nacional de Medio Ambiente: un reconocimiento merecido
    Ríos imposibles: las 171.000 barreras que rompen el curso de agua en España
    La UE abraza las renovables para romper la dependencia de Rusia
    La lucha en un pueblo de Teruel para salvar su última montaña
    ¿Qué aire respiran los niños de Madrid y Barcelona? En el 46% de los colegios se supera la contaminación permitida
    Así se puede ver la alineación de cinco planetas a simple vista, justo antes de cada amanecer
    Las vacunas contra el coronavirus salvaron 20 millones de vidas en su primer año
    Seis jóvenes científicos que han impulsado avances en la investigación matemática de vanguardia obtienen los Premios Vicent Caselles
    Así se puede ver la alineación de cinco planetas a simple vista, justo antes de cada amanecer 
    Fracciones egipcias
    El Congreso aprueba la reforma de la ley de la ciencia sin votos en contra
    Matemáticas para describir los remolinos, los taxis del océano
    Las incógnitas de la pastilla milagrosa contra un tipo de calvicie
    ¿Se puede dejar de roncar?
    El síndrome del hombre lobo y la realidad lógica de su fábula
    Muere Yves Coppens, uno de los descubridores del fósil más famoso del mundo 
    Ni patentes, ni firmar estudios: las científicas reciben mucho menos reconocimiento por su trabajo
    La metástasis del cáncer avanza durante el sueño
    A la caza de exolunas, la próxima frontera de exploración planetaria
    Hachas, niños y asesinatos bajo césped artificial: así es la necrópolis monumental más antigua de España 
    Eloísa del Pino sustituye a Rosa Menéndez al frente del CSIC
    A la caza de exolunas, la próxima frontera de exploración planetaria
    Matemáticas para describir los remolinos, los taxis del océano
    Reaparece la tesis de María Wonenburger, la pionera matemática española que permaneció décadas en el olvido
    Técnicas criptográficas que se fundamentan en lo impredecible
    Las matemáticas de los juegos malabares
    El problema del huerto
    Números McNugget
    La moneda de Frobenius
    El síndrome del hombre lobo y la realidad lógica de su fábula
    La locura como juego; más allá del Quijote y de las novelas de Pérez Galdós
    El andar del borracho, las huellas del azar y el juego de dados en algunos libros malditos
    El campo vibratorio y las fronteras de la ciencia desde un punto de vista científico
    Paul Auster fluctuando entre el pudin de pasas y la nube de mosquitos
    ¿Son mejores las hormonas bioidénticas?
    ¿Qué surgió antes, el ARN o el ADN?
    ¿Por qué se sabe que los núcleos de la Tierra rotan?
    ¿Qué son los mini reactores nucleares?
    Invitados indeseables por Navidad: el muérdago y otras plagas que evitar durante las fiestas
    Las ‘apps’ nutricionales o cómo comer bien no debería depender de uno mismo
    Malnutrición invisible: el impacto de la pobreza en la salud infantil
    El óxido de etileno, la sustancia cancerígena que ha obligado a retirar miles de alimentos en la UE
    Que no te líen con los ingredientes: aceites y grasas de mala calidad nutricional
    Joaquín Sorolla y Esteban Vicente: cómo convertir la pasión por los jardines en luz para su arte
    Nadie quiere el cuadro de Goya
    El Museo de Teruel afirma que el Torico actual es el mismo que había antes de la Guerra Civil, que ya no era de bronce  
    “¿Cómo lo haría Tony?”
    La casa de Ana Frank: memoria del Holocausto, entre el comercio y la apropiación personal
    El libro que explica qué significa ‘votar normal’
    El poeta
    Juan Muñoz se descubre más allá de sus esculturas
    El cine quiere ser verde desde la alfombra roja a la basura de una sala
    Richard Kagan: “Mi labor no es defender o criticar la Leyenda Negra, sino entenderla”
    Gabi Ruiz, codirector del Primavera Sound: “He sido insolente, mi lugar estará ahora en segunda fila”
    ‘Elvis’, el ‘biopic’ del rey del rock, y otros estrenos de este fin de semana 
    David Cronenberg recibirá un premio Donostia 2022 del Festival de San Sebastián
    Spielberg: “John Williams es atemporal y va camino de ser eterno”
    El Ministerio de Cultura y Deporte crea el Premio Nacional de Patrimonio Cinematográfico y Audiovisual
    ¿Es el Torico de Teruel una falsificación? La restauración tras una caída desata la sospecha de que sea una copia de la Guerra Civil
    “¿Cómo lo haría Tony?”
    La arquitecta Margarita Jover: “Me resisto a que el capital decida la forma del mundo”
    La pintora Carmen Álvarez-Coto acaba con el misterio y vuelve después de tres décadas de retiro voluntario
    La Unesco alerta sobre los ataques a más de 150 espacios culturales en Ucrania
    El último atardecer de Europa se ve solo desde este lugar. Un viaje hacia el infinito por el Camino de Fisterra-Muxía
    Un paseo fluvial con museos y otro lleno de piscinas termales. Las sorpresas de la Vía de la Plata
    Lorca, en la ciudad al margen
    El Pirineo oscense, para entrar a vivir
    Toda la lectura del verano, en el bolsillo
    Harry Potter cumple 25 años: libros para revivir la magia de Hogwarts
    Los mejores libros recientes para reír a carcajadas
    Disfruta del Festival de Teatro Clásico de Mérida
    'Territorios de vanguardia' en el Museo Reina Sofía
    Últimas funciones de 'We Will Rock You'
    Nueva edición de Cibeles de cine 
    Manzanares salva la tarde de San Juan
    La fiesta de los toros, una emocionante y apasionada polémica desde el siglo XIII
    La apabullante autoridad de Roca Rey
    José Fernando Molina gusta y abre una generosa puerta grande en su presentación en Madrid
    

### Podemos mencionar que el ejercicio se repite indefinidamente,halando todos los títulares que encuentra. 


```python

```
