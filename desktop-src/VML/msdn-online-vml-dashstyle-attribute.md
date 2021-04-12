---
title: Atributo DashStyle de VML
description: Atributo DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359034"
---
# <a name="vml-dashstyle-attribute"></a>Atributo DashStyle de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica el patrón de puntos y guiones de un trazo. Lectura/escritura **VgLineDashStyle**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *elemento* DashStyle = " *expresión* " >

**Sintaxis de script**

*Element* . DashStyle = "*expresión*"

*expresión* = de *elemento*. DashStyle

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

El atributo **DashStyle** permite al usuario especificar un patrón de guiones definido de forma personalizada. Esto se hace mediante una serie de números. Los estilos de guión se definen en términos de la longitud del guión (la parte dibujada del trazo) y la longitud del espacio entre los guiones. Las longitudes son relativas al ancho de línea: una longitud de "1" es igual al ancho de línea. El estilo **EndCap** se aplica a cada guión; el estilo de la flecha no lo es. La cadena define primero la longitud del guión y, a continuación, la longitud del espacio. Esto puede repetirse para formar estilos de guiones complejos. La cadena siempre debe contener un par de números; Si contiene un número impar de números, es posible que se descarte la última.

En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto. "0" implica un punto que debe ser fourfold simétrico (con extremos de redondeo redondeados debe ser un círculo). Si el extremo de la línea es "plano", un visor debe elegir un guion del sistema operativo integrado siempre que sea posible (en otras palabras. algo que es rápido de dibujar). En la tabla siguiente se muestran algunos ejemplos.



| DashStyle     | Descripción                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| "2 2"         | Guiones cortos. Cada guión y el espacio entre es dos veces el ancho de la línea.                        |
| "0 2"         | Suspensivos. El espacio entre es dos veces el ancho de la línea.                                                  |
| "2 2 0 2"     | Guión corto punto.                                                                                      |
| "2 2 0 2 0 2" | Breve guión punto punto.                                                                                  |
| "1 2"         | Semitono. Cada guión es el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea.            |
| "4 2"         | Dash. Cada guión es cuatro veces el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea. |
| "8 2"         | Guion largo.                                                                                           |
| "4 2 1 2"     | Guión punto.                                                                                            |
| "8 2 1 2"     | Guión largo punto.                                                                                       |
| "8 2 1 2 1 2" | Largo guión punto punto.                                                                                   |



 

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



 

 