---
title: Atributo flip de VML
description: Atributo flip de VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5293bdff5ab888b13fdc095038e74fdbcf725bbfb1948a04018fbf5a22c5677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346639"
---
# <a name="vml-flip-attribute"></a>Atributo flip de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Cambia la orientación de una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="flip: *expression* ">

**Sintaxis de script**

*element* .style.flip="*expression*"

*expresión* = *elemento*.style.flip

**Comentarios:**

Estos valores incluyen:



| Valor | Descripción                                           |
|-------|-------------------------------------------------------|
| x     | Voltee a lo largo del eje Y, invirtiendo *las x*-coordinates. |
| y     | Voltee a lo largo del eje *x,* invirtiendo las coordenadas Y. |
| xy    | Voltee a lo largo de los ejes y *y y x.*                  |
| Yx    | Voltear a lo *largo de los ejes x* e *y.*                |



 

*Atributo estándar de VML*

**Vea también**

[DvFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Ejemplo**

La forma se volteará a lo largo *del eje y* al invertir las coordenadas *x.*


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Ejemplo de atributo Flip](/previous-versions/bb229670(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 