---
title: Tipos VML básicos
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Migre las páginas web y las aplicaciones que se basan en VML en SVG u otros estándares ampliamente admitidos.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Lenguaje de marcado de vectores (VML), tipos básicos
- VML (Lenguaje de marcado de vectores), tipos básicos
- gráficos vectoriales, tipos básicos de VML
- Lenguaje de marcado de vectores (VML), tipos
- VML (Lenguaje de marcado de vectores), tipos
- gráficos vectoriales, tipos VML
- tipos VML básicos
- tipo booleano
- tipo de fracción
- tipo de ordinal
- tipo de longitud
- tipo de medida
- tipo de ángulo
- tipo de color
- tipo de fuente
- tipo de mapa de bits
- tipo de vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104557360"
---
# <a name="basic-vml-types"></a>Tipos VML básicos

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

**Contents**

-   [Introducción](#introduction)
-   [boolean](#boolean)
-   [fraction](#fraction)
-   [ordinal](#ordinate)
-   [length](#length)
    -   [Representaciones alternativas](#alternative-representations)
-   [Medi](#measure)
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
-   [tipo](#font)
-   [bitmap](#bitmap)
    -   [Formatos de archivo de imagen](#picture-file-formats)
-   [medios](#vector)

## <a name="introduction"></a>Introducción

Esta propuesta usa un pequeño número de tipos básicos, que se enumeran en la tabla siguiente.



| Tipo                  | Elemento           | Representación fundamental | Descripción                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 bit                      | Valor booleano: true o false.                                                                      |
| [fraction](#fraction) |                   | número 2 6                 | Un valor numérico, escalado por 2 6 (65536) y almacenado como un entero con signo.                               |
| [ordinal](#ordinate) |                   | signo más de entero de 30 bits   | Parte de una coordenada (por ejemplo, en una ruta de acceso), los valores definidos por coordenadas.                                |
| [length](#length)     |                   | [PERTENEZCA](#length)             | Una longitud física, como el ancho de una línea o el tamaño de una fuente.                                |
| [Medi](#measure)   |                   | UME o número 2 6          | Una longitud física, incluido un número de píxeles del dispositivo o una fracción de otra cantidad. |
| [angle](#angle)       |                   | grados 2 6                | Un ángulo; Positive es el sentido de las agujas del reloj.                                                                     |
| [color](#color)       | [c](#color)       | complejas                    | Elemento que permite derivar un color.                                                        |
| [tipo](#font)         | [tipo](#font)     | complejas                    | Descripción de una fuente.                                                                             |
| [bitmap](#bitmap)     | [bitmap](#bitmap) | href                       | Referencia a un archivo de imagen externo.                                                             |
| [medios](#vector)     | [v](#vector)      | complejas                    | Descripción de una ruta de acceso de vector                                                                       |



 

La "representación fundamental" es la representación de precisión más alta que la propuesta requiere que el mantenimiento de una implementación conforme. los datos se perderán si la implementación no puede representar los datos con la precisión requerida. Los tipos de color, fuente y Vector corresponden a los elementos que tienen la misma estructura, en cierto sentido, no son tipos básicos. sin embargo, es conveniente tratarlos como tal en esta propuesta.

Cada tipo básico no complejo tiene un elemento asociado con el mismo nombre. Estos nombres de elemento están reservados y no se pueden usar para ningún otro propósito dentro de las extensiones, incluso si el uso está dentro de un elemento de extensión de vista "SKIP". Debido a esto, es posible que una implementación que encuentra XML desconocido proporcione un almacenamiento interno eficaz del XML desconocido, siempre y cuando los valores se incluyan en los elementos "tipo".


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



En el primer ejemplo anterior, la cadena "1,578" se debe almacenar como una secuencia de caracteres (la implementación no sabe si es una cadena o un número). en el segundo ejemplo, el elemento de fracción indica que el contenido es un número, por lo que se puede convertir en la representación de fracción de precisión alta.

Los tipos complejos (incluido el mapa de bits) tienen asociados nombres de elementos que se utilizan para delimitar el valor. Esto simplifica el análisis asegurándose de que las tareas de análisis más complejas estén asociadas a etiquetas de elementos únicas.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Un valor booleano se representa como una palabra clave que indica el estado de la marca. Las palabras clave siguientes están definidas.



| Valor para true | Valor para false |
|----------------|-----------------|
| true           | false           |
| sí            | no              |
| en             | apagado             |
| t              | f               |
| 1              | 0               |



 

Una implementación puede escribir cualquier valor y debe reconocer todos los valores. Una implementación es gratuita para cambiar los valores de una representación a otra.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="fraction"></a>fraction


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Todos los valores numéricos (es decir, los valores de cantidades no dimensionales) dentro de esta propuesta se pueden almacenar como enteros si se escalan por 2 6 (65536). Se puede proporcionar un número en este formulario, con el sufijo f o como un número decimal sin sufijo. Por lo tanto, los siguientes elementos hipotéticos representan el mismo valor.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Una cantidad con el sufijo f debe ser un número entero; no se permiten números fraccionarios. El entero resultante debe ser representable como un número de complemento de 32 bits 2. por lo tanto, el intervalo efectivo de la representación es 32768 (de hecho, menor que 32768 y mayor o igual que-32768).

Se requiere una implementación compatible para conservar los valores que se expresan como valores f. Los valores representados como números decimales se pueden convertir a un valor f y almacenarlos de este modo. Una aplicación puede registrar valores generados internamente en cualquier unidad adecuada; sin embargo, un valor leído de un documento existente debe mantenerse en la precisión original completa o debe convertirse en un valor f.

Si la implementación no puede hacerlo, debe advertir al usuario de que se pueden perder datos. (Es aceptable emitir una advertencia de este tipo cuando se encuentren los datos generados externamente).

Cuando un valor decimal se convierte en formato f, la implementación puede utilizar cualquier modo de redondeo aritmético; sin embargo, un número entero se debe convertir al formato f exactamente. Se recomienda que las implementaciones se conviertan por redondeo a menos infinito y que la conversión siempre sea exacta.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="ordinate"></a>ordinal


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Las unidades del sistema de coordenadas establecido por coordenadas son de algún tipo nominal, que se conoce como ordinal. Se trata de una medida de longitud, pero solo se usa en relación con el rectángulo que establece la coordenadas. Cualquier valor de tipo ordinal se escalará con los valores *w* y *h* de la coordenadas y la relación resultante utilizada para establecer una medición real en el dispositivo de salida.

Una implementación compatible debe ser capaz de controlar valores ordinales de hasta 30 bits más signo (es decir, un entero con signo de 31 bits, no un entero con signo de 32 bits). No obstante, se recomienda que las implementaciones intenten generar coordenadas para la ruta de acceso y elementos similares que tengan aproximadamente 16 bits de precisión. Esto minimizará la posibilidad de subdesbordamiento o desbordamiento en una implementación no conforme.

los valores de ordinales son siempre integrales. Un separador decimal no puede aparecer en un valor de tipo ordinal. No se pueden anexar especificadores de unidad a valores de tipo ordinal.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Una longitud es una medida real o, a veces, una medida en píxeles del dispositivo. Se recomienda que las implementaciones eviten el uso de píxeles del dispositivo (PX).

Todos los calificadores de unidad de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) estándar se permiten en una longitud. Además, se puede usar el calificador UEM. Este calificador hace referencia a una unidad, la UME (unidad de métricas en inglés), que es un denominador común de las cantidades de medida en uso generalizado en gráficos de equipos. La UEM es de <sup>pulgada</sup> /914400, es decir, hay 914400 UME por pulgada. En la tabla siguiente se muestra el número de EMUs en un número pequeño de unidades que se encuentran normalmente.



| Número de EMUs | Número por pulgada | Número por milímetro | Descripción             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0,01                  | Win32 HIMETRIC          |
| 12700          | 72              |                       | Elija                 |
| 635            | 1440            |                       | Win32 TWIP              |
| 762            | 1200            |                       | Impresora de alta resolución |



 

No se permiten números fraccionarios de EMUs. Cualquier medida debe representarse como un número entero con signo de 32 bits de EMUs; esto limita la magnitud de una medida a 2348 pulgadas: aproximadamente 59 metros o 65 metros. Dado que las mediciones siempre hacen referencia al tamaño de una representación en un dispositivo de salida de pantalla o de tamaño de página nominal, siempre estarán dentro de este intervalo.

No obstante, tenga en cuenta que la representación no es adecuada para las mediciones del mundo real y que se registran (por ejemplo, para registrar el tamaño real de una ruta de acceso) se debe usar otra representación.

Se requiere una implementación compatible para conservar los valores que son un número exacto de EMUs. Los valores representados de otra forma se pueden convertir a un valor de UEM y almacenarse de esta manera. Una aplicación puede registrar valores generados internamente en cualquier unidad adecuada; sin embargo, un valor leído de un documento existente debe mantenerse en la precisión original completa o debe convertirse en un valor de UEM.

Si la implementación no puede hacerlo, debe advertir al usuario de que se pueden perder datos. (Es aceptable emitir una advertencia de este tipo cuando se encuentren los datos generados externamente).

En la práctica, la longitud física se usa para relativamente pocas mediciones en esta propuesta. Los datos que suelen ser más importantes son los datos de la ruta de acceso y se codifican en el sistema de coordenadas definido, de forma individual, por coordenadas.

### <a name="alternative-representations"></a>Representaciones alternativas

Las representaciones de longitud estándar de HTML se definen mediante [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) . Las unidades relativas, con la excepción del píxel, no son significativas en el contexto en el que se usan las longitudes en esta propuesta y no deben usarse. Si el documento registra el tamaño de píxel previsto (destino), define la traslación de píxeles en la UME; de lo contrario, debe usarse el valor predeterminado de 90 PPP definido por [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .

Con la excepción de la UEM, cualquier valor se puede proporcionar como una fracción decimal. Cuando se convierte un valor decimal en la UME, la implementación puede utilizar cualquier modo de redondeo aritmético. (La única manera de que una aplicación de creación garantice un resultado determinado es especificarla en la UEM).

Si no se proporciona ningún especificador de unidad en un valor de longitud, la implementación debe asumir la UME.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="measure"></a>measure


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Una medida es una cantidad que puede ser una [longitud](#length) o una [fracción](#fraction). Esto es muy parecido a las medidas de longitud de HTML y CSS, que pueden ser, en muchos casos, medidas físicas o porcentajes de otra cantidad. Si no se especifica ningún especificador de unidad, se debe suponer que el valor es una fracción decimal (por lo tanto, este comportamiento se hereda de fracción, no de longitud).

A diferencia de la longitud, un valor de píxel tiene un significado definido por el contexto, por lo que la conversión a la UME normalmente no es apropiada. Hay tres representaciones fundamentales posibles que debe mantener la implementación (es decir, una representación no se puede convertir en otra sin pérdida de información).

1.  Un valor fraccionario debe mantenerse en el formato de [fracción](#fraction) (un valor "f").
2.  Una longitud física debe mantenerse en la UEM.
3.  Un valor de píxel debe mantenerse como un número entero de píxeles.

No se permiten números fraccionarios de píxeles.

### <a name="alternative-representations"></a>Representaciones alternativas

Se permiten todas las representaciones alternativas de la [fracción](#fraction) y la [longitud](#length) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



La representación fundamental de un ángulo es un número de grados múltiplos por 2 6 (65536) y se almacena como un entero. Dado que el espacio de coordenadas se invierte (el eje y positivo está inactivo), un ángulo en el sentido de las agujas del reloj es positivo. Se requiere una implementación compatible para conservar la precisión completa de este tipo de valor.

Se permite que una implementación use cualquier intervalo para ángulos y se le permite normalise un ángulo (por ejemplo, de-180 a + 180 o 0 a 360). No es necesario que las implementaciones sean coherentes. sin embargo, la representación entera de un ángulo no debe superar el intervalo de un entero con signo de 32 bits.

El sufijo FD se usa para identificar esta representación de un ángulo (grado fraccionario). Observe que esto se distingue del sufijo f para una fracción sin dimensiones, aunque se puede usar una aritmética idéntica para admitirlo. El valor predeterminado para un valor de angular es simple degrees, es decir, un valor sin escala. Esto también puede señalizarse con el sufijo "" (el símbolo de grado); sin embargo, el uso de esto depende de tener una codificación de documento adecuada; por lo tanto, el regrado del sufijo también se define como la media de grados. El conjunto completo de posibles sufijos es como se indica a continuación.



| Sufijo       | Factor de conversión | Comentarios                               |
|--------------|-------------------|----------------------------------------|
| FD           | 1                 | Representación interna de alta precisión |
| ninguno, DEG,   | 65536             | Degrees (Grados)                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Representaciones alternativas

La transformación de escalado tiene discontinuidades en múltiplos impares de 45. Por lo tanto, es muy importante para la conversión de cualquier cantidad inexacta que esté bien definida. Por esta razón, la aritmética de la conversión se define para redondear hacia menos infinito.

Como esto puede ser difícil o imposible de garantizar en algunas implementaciones, el uso de lo siguiente se define como una característica de nivel 3:

1.  Cualquier valor de grado fraccionario.
2.  Cualquier valor en radianes

Por lo tanto, los valores calificados FD y valores enteros no calificados, o valores enteros calificados en grados o deben controlarse exactamente mediante una implementación de nivel 0 compatible. otros valores no necesitan. Se recomienda encarecidamente que cualquier implementación controle la conversión de un valor de grado fraccionario a un valor de grado escalado (FD) exactamente. Esto se puede hacer sin compatibilidad de punto flotante.

Los más requisitos de la conversión distinguen FD de f.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



Los colores son una parte esencial de los gráficos modernos del equipo. La propuesta usa los métodos establecidos para especificar colores fijos. Sin embargo, los colores de los diagramas rara vez son colores estáticos simples; a menudo se derivan de otros elementos del diagrama. Gran parte de esta información es específica de la aplicación, por lo que esta propuesta proporciona dos mecanismos muy básicos para especificar este comportamiento:

1.  Un color puede derivarse de otro color de la misma forma.
2.  Se define un pequeño número de operaciones aritméticas para derivar, o modificar, un color.

El mecanismo de forma de prototipo lo complementa gracias a que permite definir prototipos a partir de los cuales se pueden heredar los colores.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Un valor de color es un supraconjunto de la [definición de color CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) . Las extensiones permiten determinar el valor de color RGB de otros colores dentro de la forma o de una combinación de colores general definida mediante CSS1.

Si el valor de un elemento se define como un color, el *contenido* de un elemento define el valor de color por medio de un token de color único modificado opcionalmente por una operación aritmética en el color RGB correspondiente.

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="color-units"></a>Unidades de color

El conjunto completo de tokens de color procede de diversos orígenes: HTML, CSS1 y esta propuesta. Se definen como se indica a continuación mediante la notación de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) o la notación XPointer definida para la vinculación XML.

En las definiciones de XPointer, el origen de ubicación es el elemento que contiene el valor de color y la expresión hace referencia al conjunto de elementos completo de la forma como si cualquier elemento de prototipo base se hubiera combinado con la forma. Cuando el elemento correspondiente no existe, se utiliza en su lugar el valor predeterminado de ese elemento.



| Color            | Definición                                                                                                  | Nivel | Descripción                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Consulte a continuación                                                                                                   | 0     | Nombre del color HTML, como se muestra en la tabla siguiente.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Representación de color CSS1/sRGB estándar con valores en el intervalo comprendido entre 0 y 255, que se representan con 2 dígitos hexadecimales.                                                     |
| \#RGB            | \#RRGGBB                                                                                                    | 1     | Formato CSS1 reducido con solo tres dígitos hexadecimales.                                                                                                                   |
| RGB (r, g, b)       | \#c i b                                                                                                 | 1     | CSS1 forma RGB; los elementos del valor RGB se convierten tal y como se define en [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .                                      |
| fill             | antecesor (1, forma)<br/> secundario (1, relleno)<br/> secundario (1, color)<br/>                           | 1     | Color de relleno de primer plano de la forma.                                                                                                                                   |
| fillBack         | antecesor (1, forma)<br/> secundario (1, relleno)<br/> secundario (1, atrás)<br/> secundario (1, color)<br/> | 1     | Color de fondo del relleno de la forma.                                                                                                                                   |
| line             | antecesor (1, forma)<br/> secundario (1, línea)<br/> secundario (1, color)<br/>                           | 1     | Color de la línea de primer plano de la forma.                                                                                                                                   |
| lineBack         | antecesor (1, forma)<br/> secundario (1, línea)<br/> secundario (1, atrás) <br/> secundario (1, color)<br/> | 1     | Color de línea de fondo de la forma.                                                                                                                                   |
| lineOrFill       | línea, relleno                                                                                                  | 1     | Valor de línea si no se ha predeterminado; de lo contrario, el valor de relleno. Esto devuelve eficazmente el color que está en el borde de la forma.                                           |
| fillThenLine     | relleno, línea                                                                                                  | 1     | Valor de relleno si no se ha predeterminado, de lo contrario, el valor de línea. Esto devuelve el color de la forma principal (si la forma no está rellena, el resultado será el color de la línea).   |
| shadow           | antecesor (1, forma)<br/> secundario (1, sombra)<br/> secundario (1, color)<br/>                         | 2     | Color de la sombra (esta es una característica de nivel 2).                                                                                                                      |
| scheme           | Consulte a continuación                                                                                                   | 1     | Un color de esquema del esquema definido para el documento; Vea a continuación.                                                                                                       |
| esquema (*Índice*)  | Consulte a continuación                                                                                                   | 1     | *Índice* de color de esquema, empezando desde 0; Vea a continuación.                                                                                                                         |
| this             | Tácita                                                                                                     | 2     | La operación (relleno de una ruta de acceso o dibujo) se define de otra forma (por ejemplo, como un mapa de bits) y el color especifica una "modificación" a los colores de la forma implícita. |
| paleta (*Índice*) | Tácita                                                                                                     | 3     | Se comporta de la misma manera que esto, salvo que se identifica exactamente una entrada en una tabla de colores de mapa de bits. Solo se permite cuando se indica explícitamente.                             |
| ninguno             | \-                                                                                                          | 2     | Indica la ausencia de un color; se puede utilizar para cancelar una operación de dibujo que utiliza el color.                                                                          |
| sistema           | Consulte a continuación                                                                                                   | 3     | Color definido por la interfaz de usuario del sistema.                                                                                                                             |



 

Este color permite que un valor de color especifique una modificación de un color que se deriva de otra manera. en concreto, se puede especificar una sola operación para todos los colores de un mapa de bits. El color de la paleta (*Índice*) identifica una entrada determinada en un mapa de bits asignado a la paleta. El uso de esto solo se define para grabar una entrada de la tabla de colores que se debe considerar transparente en dicho mapa de bits.

La definición de un valor de color no debe hacer referencia a sí mismo, ya sea directa o indirectamente. Si se encuentra una definición de este tipo, se recomienda, pero no es necesario, que la implementación trate el valor sin definir como negro.

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="html-colors"></a>Colores HTML

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) define los siguientes dieciséis nombres de color:



Nombres de colores y valores sRGB

![Ejemplo de color negro.](images/black.gif)

Black = " \# 000000"

![Ejemplo de color verde.](images/green.gif)

Verde = " \# 008000"

![Ejemplo de color Silver.](images/silver.gif)

Silver = " \# C0C0C0"

![Ejemplo de color Lima.](images/lime.gif)

Lima = " \# 00FF00"

![Ejemplo de color gris.](images/gray.gif)

Gray = " \# 808080"

![Ejemplo de color oliva.](images/olive.gif)

Oliva = " \# 808000"

![Ejemplo de color blanco.](images/white.gif)

Blanco = " \# FFFFFF"

![Ejemplo de color YWLLOW.](images/yellow.gif)

Amarillo = " \# FFFF00"

![Ejemplo de color granate.](images/maroon.gif)

Granate = " \# 800000"

![Ejemplo de color marino.](images/navy.gif)

Navy = " \# 000080"

![Ejemplo de color rojo.](images/red.gif)

Red = " \# FF0000"

![Ejemplo de color azul.](images/blue.gif)

Blue = " \# 0000FF"

![Ejemplo de color púrpura.](images/purple.gif)

Púrpura = " \# 800080"

![Ejemplo de color verde azulado.](images/teal.gif)

Verde azulado = " \# 008080"

![Ejemplo de color Fuchsia.](images/fuchsia.gif)

Fuchsia = " \# FF00FF"

![Ejemplo de color aguamarina.](images/aqua.gif)

Aguamarina = " \# 00FFFF"



 

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="scheme-colors"></a>Colores de esquema

Los colores de esquema a los que se hace referencia en el esquema se definen en el nivel de documento mediante la etiqueta meta con un atributo de nombre de "esquema de color del tema".


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Esta etiqueta permite definir hasta ocho colores de esquema. De forma predeterminada, los colores no definidos deben ser negros. Los colores del esquema permiten cambiar la combinación de colores utilizada para un documento completo simplemente modificando el contenido de la combinación de colores del tema. Para asegurarse de que los gráficos importados de distintas aplicaciones de creación hacen un uso coherente de los colores del esquema, se definen las siguientes interpretaciones. El "uso" es una breve descripción del propósito y la columna "Descripción" proporciona detalles adicionales.



| Índice | Nombre              | Uso                         | Descripción                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | esquema. Background | Información previa                    | Color utilizado para el fondo de un gráfico (y, con frecuencia, para toda la página).                                    |
| 1     | Scheme. Text       | Texto y líneas                | Color del texto adjunto a una forma y el color de línea estándar.                                                      |
| 2     | Scheme. Shadow     | Shadows                       | Color de sombra estándar: el color que se usa normalmente para las sombras de formas.                                                     |
| 3     | Scheme. title      | Texto del título                    | Color que se va a usar para el título o el texto del título.                                                                              |
| 4     | Scheme. Fill       | Rellena                         | Color de relleno estándar: el color que se suele usar para rellenar formas.                                                          |
| 5     | Scheme. acento     | Destacado                        | Color normal "resaltado" que se usa para enfatizar un elemento importante de un gráfico.                                             |
| 6     | Scheme. HyperLink  | Acento e hipervínculo          | Color de resaltado utilizado para los hipervínculos. Se puede usar para otros fines en los que el color denota un vínculo a otra información. |
| 7     | esquema. seguido   | Hipervínculo de acento y seguido | Color de resaltado para los hipervínculos seguidos; también es adecuado para los vínculos "hacia atrás".                                         |



 

Se puede hacer referencia a un color de esquema por nombre o por índice, por lo que Scheme. Fill y Scheme (4) tienen el mismo color.

Los colores del esquema no participan en el esquema de valores predeterminados si no se especifica ningún color. Un color de relleno no especificado siempre debe interpretarse como blanco, independientemente del color del esquema color 4. Los colores de "acento" deben contrastar con los colores de fondo (0) y relleno (4), y los colores de texto y título deben tener la misma propiedad. Una técnica estándar es hacer que los acentos estén coloreados y el texto estándar no esté coloreado (normalmente, blanco o negro).

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="system-colors"></a>Colores del sistema

A veces, las aplicaciones registran colores en función de la configuración del sistema operativo dentro de los gráficos. Normalmente, son transitorios y no es necesario escribirlos. las definiciones de thesystemcolor existen únicamente para admitir esto. Un color del sistema se introduce definiendo una etiqueta adecuada en un nuevo espacio de nombres e insertando la información adecuada en el contenido del elemento.

Esta propuesta define esta etiqueta para codificar los colores de la interfaz de usuario de Windows definidos en el archivo de encabezado Winuser. h.


```HTML
win.color
<!element win.color #pcdata>
```



El contenido del elemento es un entero único que contiene el valor de la definición de COLOR correspondiente \_ de Winuser. h. Se puede adoptar una técnica similar para cualquier especificación de color específica del sistema o de la aplicación. Se recomienda encarecidamente que esta característica se use solo para la compatibilidad con versiones anteriores.

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="pure-colors"></a>Colores puros


```HTML
pure
<!elementpure empty>
```



Si el elemento <pure/> aparece en un valor de color, es una sugerencia que indica que el color no debe aproximarse mediante un patrón de interpolación. Se trata de una característica de nivel 1, y no es necesario que una implementación compatible lo respete. La designación es importante para los gráficos que se muestran en los dispositivos de resolución media, como las pantallas de vídeo, donde las características pequeñas (como las líneas) pueden producir un alias incorrecto con colores propuestos. En dispositivos como las impresoras, que normalmente traman todos los colores excepto los colores totalmente saturados, el tramado suele ser suficientemente adecuado para evitar este problema.

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="color-adjustments"></a>Ajustes de color

El color base se puede ajustar mediante operaciones aritméticas en el valor RGB. Estas operaciones se definen mediante elementos adicionales dentro del valor de color. Estos ajustes solo son útiles cuando se aplican a los colores derivados de otros elementos. Es válido especificar un ajuste de este tipo en un valor de color fijo. sin embargo, se permite a una implementación reducir esto al valor RGB correspondiente y almacenarlo en lugar del original.

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



El parámetro de las seis primeras operaciones es un valor numérico entero único en el intervalo comprendido entre 0 y 255. El ajuste se realiza en el valor RGB de 3x8bit como se indica a continuación:

1.  Si <gray/> se especifica, el valor RGB se sustituye por yyy, donde y es el valor de luminancia (y ') calculado a partir del valor sRGB en el siguiente ITU-r BT. 709. Este cálculo es:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Si se especifica una modificación de color. op, cada componente se ajusta por separado según la tabla siguiente. c es el valor del componente y p es el valor de color. parámetro.

    | Operación       | Fórmula                            |
    |-----------------|------------------------------------|
    | oscuro          | c: = CXP/255                       |
    | aclarar         | c: = 255-(255-c) XP/255           |
    | add             | c: = c + p                         |
    | restar        | c: = c-p                         |
    | reversesubtract | c: = p-c                         |
    | blackwhite      | Si c < p thenc: = 0elsec: = 255 |

    

     

    En cada caso, si el valor del componente calculado, c, supera 255, se usa 255 y si es menor que 0, se utiliza 0.

3.  Si <INVERT128/> se especifica, el valor 128 se resta o se agrega a cada componente de acuerdo con si el componente es menor que 128 o no.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Si <invert/> se especifica, cada componente se reemplaza por 255 menos el valor del componente.
    ```HTML
    c := 255-c
    ```

    

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="font"></a>fuente


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Una fuente se identifica mediante un atributo de estilo, tal como se define en la [sección 5,2 de CSS1 (propiedades de fuente)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) . El cuerpo del elemento Font es, en la actualidad, undefined, pero se puede usar en el futuro para codificar la información de fuente estándar. Las implementaciones iniciales de esta propuesta deben conservar pero no interpretar la información.

Es posible que se agregue compatibilidad en el futuro para obtener información de fuentes fuera de línea (fuentes descargables o recursos compartidos de fuentes). Esto se realizará mediante un elemento de vínculo XML dentro del contenido del elemento de fuente, asegurándose de que Compatbility hacia atrás con implementaciones iniciales.

[![volver ](images/top.gif) al principio hacia arriba](#top)

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



El elemento Bitmap permite incluir en un gráfico una referencia a un recurso de imagen fuera de línea (normalmente un mapa de bits).

el mapa de bits es una característica de nivel 1.

El atributo Behavior se puede usar para indicar cómo debe controlar el mapa de bits una aplicación de edición. El valor puede ser uno de los tokens siguientes o ambos.



| Token    | Descripción                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Separe | Marca el mapa de bits como una entidad independiente, que no se debe considerar como parte integral del documento. El mapa de bits no debe mantenerse con el documento. Si se copia el documento, no se debe copiar el mapa de bits; Si se mueve el documento, el mapa de bits no debe moverse con él. |
| original | El atributo title identifica la ubicación original del mapa de bits como una dirección URL. de lo contrario, no se especifica el significado de title.                                                                                                                                                          |



 

Estos valores son sugerencias para el comportamiento esperado. La opción independiente hace referencia al comportamiento de los datos a los que hace referencia href. Si se proporcionan tanto independiente como original, se espera que la aplicación ignore el URI de href y que se vuelva a generar el mapa de bits a partir de los datos originales. Si solo se proporciona el original, se espera que la aplicación use el URI de href para buscar el mapa de bits, pero puede proporcionar al usuario la opción de volver a generarlo.

Es válido para que el URI de href y el atributo de título tengan el mismo valor (léxico) (es adecuado si el mapa de bits al que se hace referencia no está "almacenado con" el documento). Está previsto (aunque no es necesario) que se use href para la propia copia del documento del mapa de bits, que puede eliminarse si se eliminan las formas de referencia, y ese título se usa para indicar una copia compartida. Por lo tanto, si ambos contienen el mismo valor, no hay ninguna copia específica del documento.

Las aplicaciones pueden pasar por alto la sugerencia si no caben en el modelo de almacenamiento real de los datos XML.

[![volver ](images/top.gif) al principio hacia arriba](#top)

### <a name="picture-file-formats"></a>Formatos de archivo de imagen

En el contexto de esta propuesta, los datos externos son invariablemente un mapa de bits o un archivo que se usa para generar un mapa de bits. En el nivel de representación 0, no es necesario admitir ningún formato de mapa de bits externo: las rutas de acceso solo se pueden rellenar con colores sólidos. Para representar el conjunto completo de rellenos de nivel de representación 1, deben admitirse los mapas de bits. El nivel de representación 1 incluye (solo) los formatos siguientes:

1.  JFIF, es decir, los datos de formato ISO/IEC 10918 incrustados dentro de un archivo con el encabezado JFIF (que se puede considerar como un marcador APP0 determinado después del creador de SOI) e incluye (solo) el intervalo de formatos JPEG admitidos por el código IJG V6.
2.  PNG, tal como se define en la especificación de la versión 1,0 de PNG.

El nivel de representación 2 también incluye compatibilidad para lo siguiente:

-   GIF, tal como se define en la especificación de GIF publicada por CompuServ en 1987 (normalmente denominada "GIF87a"). GIF89a también se debe admitir en este nivel, sujeto a la restricción de que los datos no deben contener ningún bloque de extensión que necesiten interpretación para mostrar el mapa de bits que no sea el requisito de extensionswithouta de control de gráficos para la entrada del usuario o un tiempo de retraso. Esto permite incluir comentarios, pero no la extensión de texto sin formato. Una aplicación puede insertar extensiones de aplicación (0x21, 0xFF) pero, con la terminología de esta propuesta, estas deben contener solo datos de edición, no de representación.

Cualquier otro formato de datos utilizado en el gráfico obliga a que el gráfico tenga al menos el nivel de edición 3 y, posiblemente, el nivel 3 de representación (si los datos son necesarios para representar el gráfico). Se recomienda que una aplicación publique los formatos que admite. Por ejemplo, Microsoft Office admite los siguientes formatos adicionales de forma nativa y, por tanto, puede escribir datos de edición en este formato:

1.  WMF--metarchivo de Windows (formato Win 3,1)
2.  EMF: metarchivo mejorado de Windows (formato Win32)
3.  PICT--Mac OS archivo PICT de QuickDraw (todas las versiones, pero sin registros de QuickTime ni otras extensiones)
4.  BMP: formato de archivo de mapa de bits de Windows, "OS/2" (BITMAPCORE), BITMAPINFO (, BITMAPV4 y BITMAPV5

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="vector"></a>vector


```HTML
v
<!element v "( #pcdata | p )*">
```



Una ruta de acceso de gráfico vectorial se codifica como Pcdata. El contenido del elemento v es mixto, que contiene una descripción de la ruta de acceso del vector opcionalmente parametrizada con p Elements.

[Volver a la información general de VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

