---
title: Atributo oned de VML
description: Atributo oned de VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef444037a0cd05a7cfbed5a97bb93ed7e8236a9d9f66bf1f7bd77b92b82e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999155"
---
# <a name="vml-oned-attribute"></a>Atributo oned de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si los identificadores adicionales de una forma están ocultos. Lectura/escritura **DvTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:oned=" *expression* ">

**Comentarios:**

Oculta todos los identificadores de forma excepto los de la parte superior izquierda y la parte inferior derecha; es decir, los mismos identificadores que se usan para un segmento de línea recta. El valor predeterminado es **False**.

*Microsoft Office Atributo Extensions*

**Ejemplo**

Se ocultan todos los identificadores de la parte superior izquierda e inferior derecha de la forma.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 