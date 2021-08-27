---
title: Atributo MSO-Wrap-Distance-Bottom de VML
description: Atributo MSO-Wrap-Distance-Bottom de VML
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e28ea0f2d84b9bf9f5981f9ebb22f15af75a2071f07dd9f3e006ac70b34256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007685"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a>Atributo MSO-Wrap-Distance-Bottom de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la distancia desde el lado inferior de la forma hasta el texto que la rodea. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="mso-wrap-distance-bottom: *expression* ">

**Comentarios:**

Tenga en cuenta que este atributo es diferente del **atributo** margen CSS. **Margin** cambia el origen de la forma para incluir las áreas de margen, pero la distancia de encapsulado en Microsoft Office no cambia el origen de la forma.

*Microsoft Office Atributo Extensions*

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



 

 