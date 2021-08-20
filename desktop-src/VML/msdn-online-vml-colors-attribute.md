---
title: Atributo colores de VML
description: Atributo colores de VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a699b0ab8da898dd82fa4e1bf4823c0f9fdd443eb8275e25dbfaac6d2f039a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999285"
---
# <a name="vml-colors-attribute"></a>Atributo colores de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define varios colores para un relleno de degradado. Lectura/escritura **IVgGradientColorArray**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* colors=" *expression* ">

**Sintaxis de script**

*element* .colors="*expression*"

*expresión* = *elemento*.colors

**Comentarios:**

Se usa para definir una matriz que consta de valores emparejados de porcentajes[(CombFracción)](msdn-online-vml-vgfraction-data-type.md)y color[(Color De color](msdn-online-vml-ivgcolor.md)). La matriz crea un relleno combinado con cada punto de la matriz, empezando por el 0 % (definido por **Color)** y finalizando en el 100 % (definido por **Color2**). Los colores intermedios a lo largo del proceso se pueden definir asignando un valor de color a un porcentaje. El porcentaje y el par de colores no están separados por una coma, pero los pares se separan entre sí mediante comas.

Atributo estándar de VML

**Ejemplo**

La forma tiene un relleno de degradado que consta de cuatro colores, empezando por el rojo, la mezcla al amarillo, después el verde y, por último, el azul.


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



 

 