---
title: Atributo de colores VML
description: Atributo de colores VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533351"
---
# <a name="vml-colors-attribute"></a>Atributo de colores VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define varios colores para un relleno de degradado. Lectura/escritura **IVgGradientColorArray**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: color de *elemento* = " *expresión* " >

**Sintaxis de script**

*Element* . Colors = "*expresión*"

*expresión* = de *Element*. Colors

**Comentarios:**

Se usa para definir una matriz formada por valores emparejados de porcentajes ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) y color ([VgColor](msdn-online-vml-ivgcolor.md)). La matriz crea un relleno mezclado usando cada punto de la matriz, empezando en 0% (definido por el **color**) y terminando en 100% (definido por el **color2**). Los colores intermedios a lo largo del proceso se pueden definir asignando un valor de color a un porcentaje. El par de porcentaje y de color no está separado por una coma, pero los pares se separan entre sí mediante comas.

Atributo estándar de VML

**Ejemplo**

La forma tiene un relleno de degradado que consta de cuatro colores, empezando por rojo, mezclado con amarillo, verde y finallyblue.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 