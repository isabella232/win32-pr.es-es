---
title: Colorear formas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web Workshop, colorear formas
- diseñar páginas web, colorear formas
- Lenguaje de marcado de vectores (VML), colorear formas
- VML (Lenguaje de marcado de vectores), formas coloreadas
- gráficos vectoriales, formas coloreadas
- Formas VML, colorear
- colorear formas
- Lenguaje de marcado de vectores (VML), nombres de colores de palabras clave
- VML (Lenguaje de marcado de vectores), nombres de colores de palabras clave
- gráficos vectoriales, nombres de colores de palabras clave
- nombres de colores de palabras clave
- Lenguaje de marcado de vectores (VML), triples RGB
- VML (Lenguaje de marcado de vectores), triples RGB
- gráficos vectoriales, triples RGB
- Triples RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078055"
---
# <a name="coloring-shapes"></a>Colorear formas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Como hemos mencionado en las secciones anteriores, puede usar "rojo" para representar un color rojo, "azul" para representar un color en azul, etc. En este tema, se muestra cómo dibujar formas en cualquier color que desee.

VML extiende la sintaxis de color HTML y CSS. Cuando el tipo de atributo de un elemento VML es color, como **fillColor** y **StrokeColor** , puede expresar el color mediante un nombre de [color de palabra clave](#keyword-color-name) o un [tripledo RGB](#rgb-triplet).

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="keyword-color-name"></a>Nombre de color de palabra clave

HTML 4,0 define una lista de nombres de colores de palabras clave. Son aguamarina, Black, Blue, Fuchsia, Gray, Green, Lima, granate, Navy, oliva, violeta, rojo, plata, verde azulado, blanco y amarillo. El valor RGB de estos 16 colores se define en la [especificación HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .

Por ejemplo, puede dibujar un rectángulo relleno con amarillo especificando `fillcolor="yellow"` y póngale un contorno azul especificando `strokecolor="blue"` , tal y como se muestra en la siguiente representación de VML:

![color1.gif (305 bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="rgb-triplet"></a>Tripledo RGB

Si el color no es un [nombre de color de palabra clave](#keyword-color-name), puede expresar el color como un tripledor decimal RGB o un tripledo hexadecimal RGB. Con los triples RGB, puede especificar valores para los componentes rojo, verde y azul del color, estableciendo cada componente en un valor comprendido entre 0 y 255 en decimal, o de 00 a FF en formato hexadecimal.

Por ejemplo, puede crear un rectángulo que se rellene con un color personalizado con un valor RGB de 253, 249, 186 en formato decimal especificando `fillcolor="rgb(253,249, 186)"` o `fillcolor="#FDF9BA"` , tal y como se muestra en la siguiente representación de VML. En hexadecimal, el valor 253 se convierte en FD, 249 se convierte en F9 y 186 se convierte en BA.

![color2.gif (305 bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Si el color RGB en hexadecimal tiene un patrón como XXYYZZ, puede abreviarlo como XYZ. Por ejemplo, " \# 66FF99" se puede escribir como " \# 6F9".

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="summary"></a>Resumen

En VML, puede representar un color en uno de los siguientes formatos:

1.  fillColor = "Blue"
2.  fillColor = "RGB (0, 0255)"
3.  fillColor = " \# 0000FF"

 

 