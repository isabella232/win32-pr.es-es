---
title: VML MSO-Wrap-Distance-el atributo inferior
description: VML MSO-Wrap-Distance-el atributo inferior
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c3ec66ae23994184227d857e269318606d9ea4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995415"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a>VML MSO-Wrap-Distance-el atributo inferior

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la distancia desde la parte inferior de la forma hasta el texto que se ajusta alrededor de ella. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "MSO-Wrap-Distance-Bottom: *expresión* " >

**Comentarios:**

Tenga en cuenta que este atributo es diferente del atributo de **margen** de CSS. **Margen** cambia el origen de la forma para incluir las áreas de margen, pero la distancia de ajuste en Microsoft Office no cambia el origen de la forma.

*Microsoft Office atributo Extensions*

**Ejemplo**

La forma tiene una distancia de ajuste inferior de 10 puntos.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 