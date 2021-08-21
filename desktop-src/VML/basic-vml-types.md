---
title: Tipos VML básicos
description: En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Migre las páginas web y las aplicaciones que se basan en VML a SVG u otros estándares ampliamente admitidos.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Lenguaje de marcado de vectores (VML),tipos básicos
- VML (Lenguaje de marcado de vectores),tipos básicos
- gráficos vectoriales, tipos de VML básicos
- Lenguaje de marcado de vectores (VML),types
- VML (Lenguaje de marcado de vectores),types
- gráficos vectoriales, tipos de VML
- tipos básicos de VML
- tipo booleano
- fraction type
- Tipo de ordinate
- tipo de longitud
- tipo de medida
- tipo de ángulo
- tipo de color
- tipo de fuente
- tipo de mapa de bits
- tipo de vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dbb2e540e809b88b446cceda9973f8988c7241cae7f4f96402a0edc7906550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347891"
---
# <a name="basic-vml-types"></a>Tipos VML básicos

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

**Contents**

-   [Introducción](#introduction)
-   [boolean](#boolean)
-   [fraction](#fraction)
-   [Coordinar](#ordinate)
-   [length](#length)
    -   [Representaciones alternativas](#alternative-representations)
-   [Medida](#measure)
    -   [Representaciones alternativas](#alternative-representations)
-   [angle](#angle)
    -   [Representaciones alternativas](#alternative-representations)
-   [color](#color)
    -   [Unidades de color](#color-units)
    -   [Colores HTML](#html-colors)
    -   [Colores de esquema](#scheme-colors)
    -   [Colores del sistema](#system-colors)
    -   [Colores puros](#pure-colors)
    -   [Ajustes de color](#color-adjustments)
-   [Fuente](#font)
-   [bitmap](#bitmap)
    -   [Formatos de archivo de imagen](#picture-file-formats)
-   [Vector](#vector)

## <a name="introduction"></a>Introducción

Esta propuesta usa un pequeño número de tipos básicos, enumerados en la tabla siguiente.



| Tipo                  | Elemento           | Representación fundamental | Descripción                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 bit                      | Valor booleano: true o false.                                                                      |
| [fraction](#fraction) |                   | número 2 6                 | Valor numérico, escalado en 2 6 (65536) y almacenado como un entero con signo.                               |
| [Coordinar](#ordinate) |                   | Entero de 30 bits más signo   | Parte de una coordenada (por ejemplo, en una ruta de acceso ), los valores definidos por coord.                                |
| [length](#length)     |                   | [Emú](#length)             | Longitud física, como el ancho de una línea o el tamaño de una fuente.                                |
| [Medida](#measure)   |                   | EMU o número 2 6          | Una longitud física, incluido un número de píxeles de dispositivo, o una fracción de alguna otra cantidad. |
| [angle](#angle)       |                   | grados 2 6                | Ángulo; positivo es en el sentido de las agujas del reloj.                                                                     |
| [color](#color)       | [c](#color)       | complejas                    | Elemento que permite derivar un color.                                                        |
| [Fuente](#font)         | [Fuente](#font)     | complejas                    | Descripción de una fuente.                                                                             |
| [bitmap](#bitmap)     | [bitmap](#bitmap) | href                       | Referencia a un archivo de imagen externo.                                                             |
| [Vector](#vector)     | [V](#vector)      | complejas                    | Descripción de una ruta de acceso vectorial                                                                       |



 

La "representación fundamental" es la representación de mayor precisión que la propuesta requiere que se mantenga una implementación conforme. Los datos se perderán si la implementación no puede representar los datos con la precisión necesaria. Los tipos de color, fuente y vector corresponden a elementos que tienen estructura; en cierto sentido, no son tipos básicos; sin embargo, es conveniente tratarlos como tal dentro de esta propuesta.

Cada tipo básico no complejo tiene un elemento asociado con el mismo nombre. Estos nombres de elemento están reservados y no se pueden usar para ningún otro propósito dentro de las extensiones, incluso si el uso está dentro de un elemento de extensión onview="skip". Por este motivo, es posible que una implementación que encuentre XML desconocido proporcione un almacenamiento interno eficaz del XML desconocido siempre y cuando los valores estén incluidos en los elementos "type".


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



En el primer ejemplo anterior, la cadena "1.578" debe almacenarse como una secuencia de caracteres (la implementación no sabe si es una cadena o un número); En el segundo ejemplo, el elemento fraction indica que el contenido es un número, por lo que se puede convertir en la representación de fracción de alta precisión.

Los tipos complejos (incluido el mapa de bits) tienen nombres de elementos asociados que se usan para delimitar el valor. Esto simplifica el análisis al garantizar que las tareas de análisis más complejas están asociadas a etiquetas de elemento únicas.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Un valor booleano se representa como una palabra clave que indica el estado de la marca. Se definen las siguientes palabras clave.



| Valor de true | Valor de false |
|----------------|-----------------|
| true           | false           |
| Sí            | No              |
| en             | apagado             |
| t              | f               |
| 1              | 0               |



 

Una implementación puede escribir cualquier valor y debe reconocer todos los valores. Una implementación es libre de cambiar los valores de una representación a otra.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="fraction"></a>fraction


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Todos los valores numéricos (es decir, valores de cantidades sin dimensiones) de esta propuesta se pueden almacenar como enteros si se escalan en 2 6 (65536). Se puede dar un número en este formato, con el sufijo f o como un número decimal sin sufijo. Por lo tanto, los siguientes elementos hipotéticos representan el mismo valor.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Una cantidad con el sufijo f debe ser un número entero; No se permiten números fraccionales. El entero resultante debe ser representable como un número con signo de complemento de 32 bits 2; Por lo tanto, el intervalo efectivo de la representación es 32768 (de hecho, menor que 32768 y mayor o igual que -32768).

Se requiere una implementación conforme para conservar los valores que se expresan como valores f. Los valores representados como números decimales se pueden convertir en un valor f y almacenarse de esa manera. Una aplicación puede registrar valores generados internamente en cualquier unidad adecuada. sin embargo, un valor leído de un documento existente debe mantenerse con la precisión original completa o debe convertirse en un valor f.

Si la implementación no puede hacerlo, debe advertir al usuario de que se pueden perder datos. (Es aceptable emitir esta advertencia una vez cuando se encuentran por primera vez los datos generados externamente).

Cuando un valor decimal se convierte al formato f, la implementación puede usar cualquier modo de redondeo aritmético; sin embargo, un número entero debe convertirse exactamente al formato f. Se recomienda que las implementaciones se conviertan redondeando a menos infinito y que la conversión siempre sea exacta.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="ordinate"></a>Coordinar


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Las unidades del sistema de coordenadas establecidas por coord son de algún tipo nominal, lo que se conoce como ordinate. Se trata de una medida de longitud, pero solo se usa en relación con el rectángulo que establece coord. Cualquier valor de ordinate de tipo se escalará mediante los valores *w* y *h* del coord y la relación resultante utilizada para establecer una medida real en el dispositivo de salida.

Una implementación conforme debe ser capaz de controlar valores de ordinación de hasta 30 bits más signo (es decir, un entero de 31 bits con signo, no un entero de 32 bits con signo). Sin embargo, se recomienda que las implementaciones intenten generar coordenadas para la ruta de acceso y elementos similares que tengan aproximadamente 16 bits de precisión. Esto minimizará la posibilidad de subdesbordar o desbordarse en una implementación no conforme.

Los valores ordinate siempre son enteros. Es posible que un separador decimal no aparezca en un valor de tipo ordinate. No se puede anexar ningún especificador de unidad a valores de tipo ordinate.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Una longitud es una medida real o, a veces, una medida en píxeles de dispositivo. Se recomienda que las implementaciones eviten el uso de píxeles de dispositivo (px).

Se permiten todos los [calificadores de unidad CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) estándar en una longitud. Además, se puede usar el calificador emu. Este calificador hace referencia a una unidad , la EMU (unidad métrica en inglés), que es un denominador común de las cantidades de medida en uso generalizado en gráficos informáticos. La EMU es inch/914400, es decir, hay 914400 EMU por pulgada. <sup></sup> En la tabla siguiente se muestra el número de unidades emus en un pequeño número de unidades que se encuentran habitualmente.



| Número de EME | Número por pulgada | Número por milímetro | Descripción             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0,01                  | Win32 HIMETRIC          |
| 12700          | 72              |                       | "point"                 |
| 635            | 1440            |                       | Win32 TWIP              |
| 762            | 1200            |                       | Impresora de alta resolución |



 

No se permiten números fraccionario de EME. Cualquier medida debe representarse como un número entero de EME con firma de 32 bits ( esto limita la magnitud de una medida a 2348 pulgadas ), unos 59 metros o 65 desenlazar. Dado que las medidas siempre hacen referencia al tamaño de una representación en un dispositivo de salida nominalmente de pantalla o de tamaño de página, siempre estarán dentro de este intervalo.

Sin embargo, tenga en cuenta que la representación no es adecuada para las medidas del mundo real y que, cuando se registran (por ejemplo, para registrar el tamaño real de una ruta de acceso), se debe usar otra representación.

Se requiere una implementación conforme para conservar los valores que son números exactos de EME. Los valores representados de cualquier otra manera se pueden convertir en un valor de EMU y almacenarse de esa manera. Una aplicación puede registrar valores generados internamente en cualquier unidad adecuada. sin embargo, un valor leído de un documento existente debe mantenerse con la precisión original completa o debe convertirse en un valor de EMU.

Si la implementación no puede hacerlo, debe advertir al usuario de que se pueden perder datos. (Es aceptable emitir esta advertencia una vez cuando se encuentran por primera vez los datos generados externamente).

En la práctica, las longitudes físicas se usan para relativamente pocas medidas en esta propuesta. Los datos que normalmente son más importantes son los datos de ruta de acceso y se codifican en el sistema de coordenadas definido, por forma, por coord.

### <a name="alternative-representations"></a>Representaciones alternativas

CSS1 define las representaciones de longitud estándar [de HTML.](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) Las unidades relativas, a excepción del píxel, no son significativas en el contexto en el que se usan las longitudes en esta propuesta y no se deben usar. Si el documento registra el tamaño de píxel previsto (destino), esto define la traducción de píxeles en EMU; De lo contrario, se debe usar el valor predeterminado de 90 ppp definido por [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units)

A excepción de emu, cualquier valor se puede dar como una fracción decimal. Cuando un valor decimal se convierte en EMU, la implementación puede usar cualquier modo de redondeo aritmético. (La única manera de que una aplicación de creación garantice un resultado determinado es especificarlo en emu).

Si no se especifica ningún especificador de unidad en un valor de longitud, la implementación debe asumir emu.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="measure"></a>measure


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Una medida es una cantidad que puede ser una [longitud o](#length) una [fracción](#fraction). Esto se parece estrechamente a las medidas de longitud HTML y CSS, que pueden, en muchos casos, ser medidas físicas o porcentajes de alguna otra cantidad. Si no se especifica ningún especificador de unidad, se debe suponer que el valor es una fracción decimal (por lo tanto, este comportamiento se hereda de fraction, no de length).

A diferencia de la longitud, un valor de píxel tiene un significado definido por el contexto, por lo que la conversión a emu normalmente no es apropiada. Hay tres representaciones fundamentales posibles que la implementación debe mantener (es decir, una representación no se puede convertir en otra sin pérdida de información).

1.  Se debe mantener un valor fraccionrio en formato [de](#fraction) fracción (un valor "f").
2.  Se debe mantener una longitud física en EMU.
3.  Un valor de píxel debe mantenerse como un número entero de píxeles.

No se permiten números fraccionales de píxeles.

### <a name="alternative-representations"></a>Representaciones alternativas

Se permiten todas las representaciones alternativas de [fracción](#fraction) [y](#length) longitud.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



La representación fundamental de un ángulo es un número de grados múltiplo por 2 6 (65536) y almacenado como un entero. Dado que el espacio de coordenadas se invierte (el eje y positivo está hacia abajo), un ángulo en el sentido de las agujas del reloj es positivo. Se requiere una implementación conforme para conservar la precisión completa de este valor.

Una implementación puede usar cualquier intervalo para los ángulos y se permite normalizar un ángulo (por ejemplo, de -180 a +180 o de 0 a 360). No es necesario que las implementaciones sean coherentes; sin embargo, la representación integral de un ángulo no debe superar el intervalo de un entero de 32 bits con signo.

El sufijo fd se usa para identificar esta representación de un ángulo (grado fraccional). Tenga en cuenta que esto se distingue del sufijo f para una fracción sin dimensiones, aunque se pueden usar aritméticas idénticas para admitirla. El valor predeterminado de un valor angular es grados simples, es decir, un valor sin escalar. Esto también se puede señalar con el sufijo " " (el símbolo de grado); Sin embargo, el uso de esto depende de tener una codificación de documento adecuada; por lo tanto, el sufijo deg también se define como grados medios. El conjunto completo de posibles son los siguientes.



| Sufijo       | Factor de conversión | Comentarios                               |
|--------------|-------------------|----------------------------------------|
| Fd           | 1                 | Representación interna de alta precisión |
| none, deg,   | 65536             | Degrees (Grados)                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Representaciones alternativas

La transformación de escalado tiene discontinuidades en múltiplo impar de 45 . Por lo tanto, es muy importante que la conversión de cualquier cantidad inexacta esté bien definida. Por esta razón, la aritmética de conversión se define para redondear hacia el infinito menos.

Dado que esto puede ser difícil o imposible de garantizar en algunas implementaciones, el uso de lo siguiente se define como una característica de nivel 3:

1.  Cualquier valor de grado fraccional.
2.  Cualquier valor de base

Por lo tanto, los valores fd calificados y los valores enteros no calificados, o valores enteros calificados deg o deben controlarse exactamente mediante una implementación de nivel 0 conforme; otros valores no necesitan. Se recomienda encarecidamente que cualquier implementación controle la conversión de un valor de grado fraccionado a un valor de grado escalado (fd) exactamente. Esto se puede hacer sin compatibilidad de punto flotante.

Los requisitos más exactos para la conversión distinguen fd de f.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



Los colores son una parte esencial de los gráficos de equipos modernos. La propuesta usa los métodos establecidos para especificar colores fijos. Sin embargo, los colores de los diagramas rara vez son colores estáticos simples; a menudo se derivan de otros elementos del diagrama. Gran parte de esta información es muy específica de la aplicación, por lo que esta propuesta proporciona dos mecanismos muy básicos para especificar este comportamiento:

1.  Un color puede derivarse de otro color de la misma forma.
2.  Se define un número pequeño de operaciones aritméticas para derivar o modificar un color.

El mecanismo de forma del prototipo complementa esto al permitir que se definan prototipos de los que se pueden heredar colores.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Un valor de color es un superconjunto de la [definición de color CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) . Las extensiones permiten determinar el valor de color RGB a partir de otros colores dentro de la forma o a partir de una combinación de colores general definida mediante CSS1.

Si el valor de un elemento se define  como un color, el contenido de un elemento define el valor de color mediante un token de color único modificado opcionalmente por una operación aritmética en el color RGB correspondiente.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

### <a name="color-units"></a>Unidades de color

El conjunto completo de tokens de color procede de diversos orígenes: HTML, CSS1 y esta propuesta. Se definen de la siguiente manera mediante la notación de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) o la notación XPointer definida para la vinculación XML.

En las definiciones de XPointer, el origen de ubicación es el elemento que contiene el valor de color y la expresión hace referencia a todo el conjunto de elementos de la forma como si los elementos de prototipo base se hubieran combinado con la forma. Cuando el elemento correspondiente no existe, el valor predeterminado de ese elemento se usa en su lugar.



| Color            | Definición                                                                                                  | Nivel | Descripción                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Consulte a continuación                                                                                                   | 0     | Nombre de color HTML, como se muestra en la tabla siguiente.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Representación de color CSS1/sRGB estándar mediante valores del intervalo 0..255 representados con 2 dígitos hexadecimales cada uno.                                                     |
| \#Rgb            | \#rrggbb                                                                                                    | 1     | Formulario CSS1 abreviado con solo tres dígitos hexadecimales.                                                                                                                   |
| rgb(r,g,b)       | \#(r) (g) (b)                                                                                                 | 1     | Forma rgb css1; Los elementos del valor rgb se convierten tal como se define en [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units)                                      |
| fill             | antecesor(1,forma)<br/> child(1, fill)<br/> child(1, color)<br/>                           | 1     | Color de relleno de primer plano de la forma.                                                                                                                                   |
| fillBack         | antecesor(1,forma)<br/> child(1, fill)<br/> child(1, back)<br/> child(1, color)<br/> | 1     | Color de fondo del relleno de la forma.                                                                                                                                   |
| line             | antecesor(1,forma)<br/> child(1, line)<br/> child(1, color)<br/>                           | 1     | Color de línea de primer plano de la forma.                                                                                                                                   |
| lineBack         | antecesor(1,forma)<br/> child(1, line)<br/> child(1,back) <br/> child(1, color)<br/> | 1     | Color de línea de fondo de la forma.                                                                                                                                   |
| lineOrFill       | línea, relleno                                                                                                  | 1     | Valor de línea si no está predeterminado; de lo contrario, el valor de relleno. Esto devuelve eficazmente el color que está en el borde de la forma.                                           |
| fillThenLine     | fill, line                                                                                                  | 1     | Valor de relleno si no tiene el valor predeterminado; de lo contrario, el valor de línea. Esto devuelve de forma eficaz el color de la forma principal (si la forma no se rellena, el resultado será el color de línea).   |
| shadow           | ancestor(1,shape)<br/> child(1, shadow)<br/> child(1, color)<br/>                         | 2     | Color de la sombra (se trata de una característica de nivel 2).                                                                                                                      |
| scheme           | Consulte a continuación                                                                                                   | 1     | Color de esquema del esquema definido para el documento; vea a continuación.                                                                                                       |
| scheme(*index*)  | Consulte a continuación                                                                                                   | 1     | Índice de color *de* esquema , a partir de 0; vea a continuación.                                                                                                                         |
| this             | Implícita                                                                                                     | 2     | La operación (rellenar una ruta de acceso o dibujarla) se define de alguna otra manera (por ejemplo, como un mapa de bits) y el color especifica una "modificación" de los colores tan implícitos. |
| palette(*index*) | Implícita                                                                                                     | 3     | Se comporta de la misma manera que esto, salvo que se identifica exactamente una entrada en una tabla de colores de mapa de bits. Solo se permite cuando se indica explícitamente.                             |
| ninguno             | \-                                                                                                          | 2     | Indica la ausencia de un color; se puede usar para cancelar una operación de dibujo que usa el color .                                                                          |
| sistema           | Consulte a continuación                                                                                                   | 3     | Color definido por la interfaz de usuario del sistema.                                                                                                                             |



 

Este color permite a un valor de color especificar una modificación de un color que se deriva de alguna otra manera; en concreto, se puede especificar una única operación para todos los colores de un mapa de bits. El color palette(*index*) identifica una entrada determinada en un mapa de bits asignado a la paleta. El uso de esto solo se define para registrar una entrada de tabla de colores que debe considerarse transparente en este tipo de mapa de bits.

La definición de un valor de color no debe hacer referencia a sí misma, directa o indirectamente. Si se encuentra esta definición, se recomienda, pero no es necesario, que la implementación trate el valor indefinido como negro.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

### <a name="html-colors"></a>Colores HTML

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) define los siguientes dieciséis nombres de color:



Nombres de color y valores sRGB

![Ejemplo de color negro.](images/black.gif)

Negro = " \# 000000"

![Ejemplo de color verde.](images/green.gif)

Verde = " \# 008000"

![Ejemplo de color plata.](images/silver.gif)

Silver = " \# C0C0C0"

![Ejemplo de color blanco.](images/lime.gif)

Lime = " \# 00FF00"

![Ejemplo de color gris.](images/gray.gif)

Gris = " \# 808080"

![Ejemplo de color verde blanco.](images/olive.gif)

Verde = " \# 808000"

![Ejemplo de color blanco.](images/white.gif)

White = " \# FFFFFF"

![Ejemplo de color ywllow.](images/yellow.gif)

Yellow = " \# FFFF00"

![Ejemplo de color maroon.](images/maroon.gif)

Maroon = " \# 800000"

![Ejemplo de color azul azulado.](images/navy.gif)

Azul = " \# 000080"

![Ejemplo de color rojo.](images/red.gif)

Rojo = " \# FF0000"

![Ejemplo de color azul.](images/blue.gif)

Blue = " \# 0000FF"

![Ejemplo de color púrpura.](images/purple.gif)

Púrpura = " \# 800080"

![Ejemplo de color azulado.](images/teal.gif)

Teal = " \# 008080"

![Ejemplo de color de miia.](images/fuchsia.gif)

Ffia = " \# FF00FF"

![Ejemplo de color agua acuar.](images/aqua.gif)

Aqua = " \# 00FFFF"



 

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

### <a name="scheme-colors"></a>Colores de esquema

Los colores de esquema a los que hace referencia scheme se definen en el nivel de documento mediante la metaetiqueta con un atributo name de "Theme Color Scheme".


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Esta etiqueta permite definir hasta ocho colores de esquema. Los colores no definidos deben ser de color negro de forma predeterminada. Los colores de esquema permiten cambiar la combinación de colores utilizada para un documento completo solo modificando el contenido de la combinación de colores del tema. Para asegurarse de que los gráficos importados desde diferentes aplicaciones de creación hacen un uso coherente de los colores del esquema, se definen las interpretaciones siguientes. El "uso" es una breve descripción del propósito y la columna "descripción" proporciona detalles adicionales.



| Índice | Nombre              | Uso                         | Descripción                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | scheme.background | Información previa                    | Color utilizado para el fondo de un gráfico (y, con frecuencia, para toda la página).                                    |
| 1     | scheme.text       | Texto y líneas                | Color del texto asociado a una forma y color de línea estándar.                                                      |
| 2     | scheme.shadow     | Shadows                       | Color de sombra estándar: el color que se usa normalmente para las sombras de forma.                                                     |
| 3     | scheme.title      | Texto del título                    | Color que se va a usar para el texto de título o encabezado.                                                                              |
| 4     | scheme.fill       | Llena                         | Color de relleno estándar: el color que se usa normalmente para rellenar formas.                                                          |
| 5     | scheme.accent     | Acento                        | Color "resaltado" normal que se usa para resaltar un elemento importante de un gráfico.                                             |
| 6     | scheme.hyperlink  | Acento e hipervínculo          | Resaltar el color que se usa para los hipervínculos. Se puede usar para otros fines en los que el color denota un vínculo a otra información. |
| 7     | scheme.followed   | Hipervínculo acentuable y seguido | Resaltar el color de los hipervínculos seguidos; también es adecuado para los vínculos "hacia atrás".                                         |



 

Se puede hacer referencia a un color de esquema por nombre o por índice, por lo que scheme.fill y scheme(4) tienen el mismo color.

Los colores de esquema no participan en el esquema predeterminado si no se especifica un color. Un color de relleno no especificado siempre debe interpretarse como blanco, independientemente del color del color de esquema 4. Los colores de "acento" deben contrastar con los colores de fondo (0) y relleno (4), y los colores de texto y texto del título deben tener la misma propiedad. Una técnica estándar consiste en hacer que los acentos se coloreen y el texto estándar no esté coloreado (normalmente en blanco o negro).

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

### <a name="system-colors"></a>Colores del sistema

A veces, las aplicaciones registran colores en función de la configuración del sistema operativo dentro de los gráficos. Normalmente, son transitorios y no es necesario escribir; las definiciones desystemcolor existen únicamente para admitir esto. Un color del sistema se introduce definiendo una etiqueta adecuada en un nuevo espacio de nombres e insertando la información adecuada en el contenido del elemento.

Esta propuesta define este tipo de etiqueta para codificar los colores Windows interfaz de usuario definidos en el archivo de encabezado winuser.h.


```HTML
win.color
<!element win.color #pcdata>
```



El contenido del elemento es un único entero que contiene el valor de la definición de COLOR \_ pertinente de winuser.h. Se puede adoptar una técnica similar para cualquier especificación de color específica del sistema o de la aplicación. Se recomienda encarecidamente que esta característica solo se utilice para la compatibilidad con versiones anteriores.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

### <a name="pure-colors"></a>Colores puros


```HTML
pure
<!elementpure empty>
```



Si el elemento aparece en un valor de color, es una sugerencia de que un patrón de dither no debe aproximar <pure/> el color. Se trata de una característica de nivel 1 y una implementación conforme no necesita respetarla. La designación es importante para los gráficos que se muestran en dispositivos de resolución media, como las pantallas de vídeo, donde las características pequeñas (como las líneas) pueden provocar un alias con colores de trama. En dispositivos como impresoras, que normalmente dite todos los colores excepto los pocos colores totalmente saturados, el dithering suele ser lo suficientemente adecuado para evitar este problema.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

### <a name="color-adjustments"></a>Ajustes de color

El color base se puede ajustar mediante operaciones aritméticas en el valor RGB. Estas operaciones se definen mediante elementos adicionales dentro del valor de color. Estos ajustes solo son útiles cuando se aplican a los colores derivados de otros elementos. Es válido especificar este ajuste en un valor de color fijo; Sin embargo, una implementación puede reducir esto al valor RGB correspondiente y almacenarlo en lugar del original.

Todas las características de ajuste de color descritas en esta sección son características de nivel 1.


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



El parámetro de las seis primeras operaciones es un único valor numérico entero en el intervalo de 0 a 255. El ajuste se realiza en el valor RGB de 3x8 bits como se muestra a continuación:

1.  Si se especifica , el valor RGB se reemplaza por yyy, donde y es el valor de luminance (y') calculado a partir del valor sRGB en después de <gray/> ITU-r BT.709. Este cálculo es:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Si se da una modificación de color.op, cada componente se ajusta por separado según la tabla siguiente. c es el valor del componente y p es el valor color.parameter.

    | Operación       | Fórmula                            |
    |-----------------|------------------------------------|
    | Oscurecer          | c := cxp/255                       |
    | Aligerar         | c := 255 - (255-c)xp/255           |
    | add             | c := c + p                         |
    | restar        | c := c - p                         |
    | reversesubtract | c := p - c                         |
    | Blackwhite      | si c < p thenc := 0elsec := 255 |

    

     

    En cada caso, si el valor del componente calculado, c, supera 255, se usa 255 y, si es menor que 0, se usa 0.

3.  Si se da, el valor 128 se resta o se agrega a cada componente en función de si el componente es menor <INVERT128/> que 128 o no.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Si <invert/> se da, cada componente se reemplaza por 255 menos el valor del componente.
    ```HTML
    c := 255-c
    ```

    

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="font"></a>fuente


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Una fuente se identifica mediante un atributo de estilo tal como se define en la sección [CSS1 5.2 (propiedades de fuente).](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) El cuerpo del elemento de fuente es, en la actualidad, indefinido, pero se puede usar en el futuro para codificar información de fuente estándar. Las implementaciones iniciales de esta propuesta deben conservar la información, pero no interpretarla.

Es posible que se pueda agregar compatibilidad en el futuro para la información de fuentes fuera de línea (fuentes descargables o recursos de fuente compartidos). Esto se hará mediante un elemento de vínculo XML dentro del contenido del elemento de fuente, lo que garantiza la compatibilidad con versiones anteriores con implementaciones iniciales.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="bitmap"></a>bitmap


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



El elemento de mapa de bits permite incluir una referencia a un recurso de imagen fuera de línea (normalmente un mapa de bits) en un gráfico.

bitmap es una característica de nivel 1.

El atributo de comportamiento puede usarse para indicar cómo debe controlarse el mapa de bits una aplicación de edición. El valor puede ser uno o ambos de los tokens siguientes.



| Token    | Descripción                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Separado | Marca el mapa de bits como una entidad independiente, que no debe considerarse una parte integral del documento. El mapa de bits no debe conservarse con el documento. Si se copia el documento, no se debe copiar el mapa de bits; si se mueve el documento, el mapa de bits no se debe mover con él. |
| original | El atributo title identifica la ubicación original del mapa de bits como una dirección URL; de lo contrario, no se especifica el significado del título.                                                                                                                                                          |



 

Estos valores son sugerencias en cuanto al comportamiento esperado. La opción independiente hace referencia al comportamiento de los datos a los que hace referencia href. Si se dan los elementos independiente y original, se espera que la aplicación omita el URI de href y vuelva a generar el mapa de bits a partir de los datos originales. Si solo se da original, se espera que la aplicación use el URI href para encontrar el mapa de bits, pero puede dar al usuario la opción de volver a generarlo.

Es válido hacer que el URI de href y el atributo title tenga el mismo valor (léxico): esto es adecuado si el mapa de bits al que se hace referencia no está "almacenado con" el documento. Está pensado (aunque no es necesario) que href se utilice para la propia copia del mapa de bits del documento (que se puede eliminar si se eliminan las formas de referencia) y que el título se utilice para indicar una copia compartida. Por lo tanto, si ambos contienen el mismo valor, no hay ninguna copia específica del documento.

Las aplicaciones pueden pasar por alto la sugerencia si no encaja con el modelo de almacenamiento real de los datos XML.

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

### <a name="picture-file-formats"></a>Formatos de archivo de imagen

En el contexto de esta propuesta, los datos externos son invariablemente un mapa de bits o un archivo que se usa para generar un mapa de bits. En el nivel de representación 0, no es necesario que se admite ningún formato de mapa de bits externo; las rutas de acceso solo se pueden rellenar con colores sólidos. Para representar el conjunto completo de rellenos de nivel de representación 1, deben ser compatibles los mapas de bits. El nivel de representación 1 incluye (solo) los siguientes formatos:

1.  JFIF, es decir, datos de formato ISO/IEC 10918 insertados en un archivo con el encabezado JFIF (que se puede considerar como un marcador APP0 determinado después del creador de SOI) e incluyendo (solo) el intervalo de formatos JPEG admitidos por el código IJG v6.
2.  PNG, tal como se define en la especificación PNG versión 1.0.

El nivel de representación 2 también incluye compatibilidad con lo siguiente:

-   GIF, tal como se define en la especificación GIF publicada por CompuServ en 1987 (normalmente denominada "GIF87a"). GIF89a también debe ser compatible en este nivel, sujeto a la restricción de que los datos no deben contener bloques de extensión que necesiten interpretación para mostrar el mapa de bits distinto de las extensiones de control de gráficos sin ningún requisito para la entrada del usuario o un tiempo de retraso. Esto permite incluir comentarios, pero no la extensión de texto sin formato. Una aplicación puede insertar extensiones de aplicación (0x21, 0xFF), pero, mediante la terminología de esta propuesta, solo deben contener datos de edición, no representación.

Cualquier otro formato de datos usado en el gráfico obliga a que ese gráfico sea al menos el nivel de edición 3 y, posiblemente, el nivel 3 (si los datos son necesarios para representar el gráfico). Se recomienda que una aplicación publique los formatos que admite. Por ejemplo, Microsoft Office admite los siguientes formatos adicionales de forma nativa y, por tanto, puede escribir datos de edición de este formato:

1.  WMF: Windows metarchivo (formato Win 3.1)
2.  EMF: Windows metarchivo "mejorado" (formato Win32)
3.  ASÍNto: Mac OS quickdraw de CSV (todas las versiones, pero sin registros QuickTime ni otras extensiones)
4.  BMP: formato Windows archivo de mapa de bits, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 y BITMAPV5

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

## <a name="vector"></a>vector


```HTML
v
<!element v "( #pcdata | p )*">
```



Una ruta de acceso gráfica vectorial se codifica como pcdata. El contenido del elemento v es mixto, que contiene una descripción de ruta de acceso vectorial con parámetros opcionales con elementos p.

[Vuelva a la introducción a VML.](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

