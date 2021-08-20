---
title: Colores de formas
description: En este artículo se describe la coloración de formas en VML, una característica que está en desuso a partir Windows Internet Explorer 9.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Taller web, colores de formas
- diseñar páginas web, colorear formas
- Lenguaje de marcado de vectores (VML),formas para colorear
- VML (Lenguaje de marcado de vectores), formas para colorear
- gráficos vectoriales, formas para colorear
- Formas de VML, coloreo
- formas para colorear
- Lenguaje de marcado de vectores (VML),nombres de color de palabra clave
- VML (Lenguaje de marcado de vectores),nombres de color de palabra clave
- gráficos vectoriales, nombres de color de palabra clave
- nombres de color de palabra clave
- Lenguaje de marcado de vectores (VML), trillizos RGB
- VML (Lenguaje de marcado de vectores), tripletes RGB
- gráficos vectoriales, tripletes RGB
- Tripletes RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edd8b067f1e3648d2b69f473c02c59392a10b5716afea74b8f7b0c9d093989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057056"
---
# <a name="coloring-shapes"></a>Colores de formas

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como se mencionó en secciones anteriores, puede usar "rojo" para representar un color en rojo, "azul" para representar un color en azul, y así sucesivamente. En este tema, se ilustrará cómo dibujar formas en el color que desee.

VML amplía la sintaxis de color HTML y CSS. Cuando el tipo de atributo de un elemento VML es color (como **fillcolor** y **strokecolor),** puede expresar el color mediante un nombre de [color](#keyword-color-name) de palabra clave o un [triplete RGB](#rgb-triplet).

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="keyword-color-name"></a>Nombre de color de palabra clave

HTML 4.0 define una lista de nombres de color de palabra clave. Son aqua, black, blue, brewia, gray, green, lime, maroon, black, purple, red, silver, teal, white y yellow. El valor RGB de estos 16 colores se define en la [especificación HTML 4.0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .

Por ejemplo, puede dibujar un rectángulo relleno de amarillo especificando y darle un contorno azul mediante la especificación de , como se muestra en la siguiente representación `fillcolor="yellow"` `strokecolor="blue"` de VML:

![color1.gif (305 bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="rgb-triplet"></a>Triplete RGB

Si el color no es un nombre [de color](#keyword-color-name)de palabra clave, puede expresar el color como un triplete decimal RGB o un triplete hexadecimal RGB. Con los tripletes RGB, puede especificar valores para los componentes rojo, verde y azul del color, estableciendo cada componente en un valor que va de 0 a 255 en decimal o de 00 a FF en hexadecimal.

Por ejemplo, puede crear un rectángulo que se rellena con un color personalizado con un valor RGB de 253, 249, 186 en decimal especificando o , como se muestra en la siguiente representación `fillcolor="rgb(253,249, 186)"` `fillcolor="#FDF9BA"` de VML. En hexadecimal, el valor 253 se convierte en FD, 249 se convierte en F9 y 186 se convierte en BA.

![color2.gif (305 bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Si rgb en hexadecimal tiene un patrón como XXYYZZ, puede abreviar a XYZ. Por ejemplo, \# "66FF99" se puede escribir como \# "6F9".

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="summary"></a>Resumen

En VML, puede representar un color en uno de los formatos siguientes:

1.  fillcolor="blue"
2.  fillcolor="rgb(0,0,255)"
3.  fillcolor=" \# 0000ff"

 

 