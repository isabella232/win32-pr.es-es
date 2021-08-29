---
title: Atributo DashStyle de VML
description: Atributo DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ad1aabbf26e1aa5b7f2b1c9155ed137d23c8563924f41230f60e6415ac10d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007864"
---
# <a name="vml-dashstyle-attribute"></a>Atributo DashStyle de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el patrón de punto y guion para un trazo. Lectura/escritura **BvLineDashStyle**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* dashstyle=" *expression* ">

**Sintaxis de script**

*element* .dashstyle="*expression*"

*expresión* = *elemento*.dashstyle

**Comentarios:**

Estos valores incluyen:

-   Solid (predeterminado)
-   ShortDash
-   ShortDot
-   ShortDashDot
-   ShortDashDotDot
-   Punto
-   Guión
-   LongDash
-   DashDot
-   LongDashDot
-   LongDashDotDot

El **atributo DashStyle** permite al usuario especificar un patrón de guion definido de forma personalizada. Esto se hace mediante una serie de números. Los estilos de guion se definen en términos de la longitud del guión (la parte dibujada del trazo) y la longitud del espacio entre los guiones. Las longitudes son relativas al ancho de línea: una longitud de "1" es igual al ancho de línea. El **estilo EndCap** se aplica a cada guión, el estilo de flecha no. La cadena define primero la longitud del guion y, a continuación, la longitud del espacio. Esto se puede repetir para formar estilos de guion complejos. La cadena siempre debe contener un par de números; si contiene un número impar de números, se puede pasar por alto el último.

En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto. "0" implica un punto que debe ser cuatro veces simétrico (con los límites de extremo round debe ser un círculo). Si el extremo de línea es "plano", un visor debe elegir un guión del sistema operativo integrado siempre que sea posible (en otras palabras. algo que es rápido de dibujar). En la tabla siguiente se muestran algunos ejemplos.



| DashStyle     | Descripción                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| "2 2"         | Guiones cortos. Cada guión y el espacio entre es el doble del ancho de la línea.                        |
| "0 2"         | Puntos. El espacio entre es el doble del ancho de la línea.                                                  |
| "2 2 0 2"     | Punto de guión corto.                                                                                      |
| "2 2 0 2 0 2" | Punto de punto de guión corto.                                                                                  |
| "1 2"         | Punto. Cada guión es el ancho de la línea, mientras que cada espacio es el doble del ancho de la línea.            |
| "4 2"         | Guión. Cada guión es cuatro veces el ancho de la línea, mientras que cada espacio es el doble del ancho de la línea. |
| "8 2"         | Guion largo.                                                                                           |
| "4 2 1 2"     | Punto de guión.                                                                                            |
| "8 2 1 2"     | Punto de guión largo.                                                                                       |
| "8 2 1 2 1 2" | Punto de punto de guion largo.                                                                                   |



 

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un estilo de guión de guiones y puntos alternos.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 