---
title: Atributo WrapCoords de VML
description: Atributo WrapCoords de VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae4d7e3c0424de58e64fb68b27b863de2b1d0bf64e23ac653f7121c891bd47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938901"
---
# <a name="vml-wrapcoords-attribute"></a>Atributo WrapCoords de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el polígono delimitador que rodea una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:wrapcoords=" *expression* ">

**Comentarios:**

Describe una lista delimitada por comas de x e ycoordinates; es decir, "x1,y1,x2,y2,x3,y3,..." Esto se usa cuando el texto se ajusta estrechamente alrededor de una forma. El valor predeterminado **es NULL** (una cadena vacía) hasta que el atributo **MSO-Wrap-Mode** se establece en **tight** o a **través de**.

*Microsoft Office Atributo Extensions*

**Ejemplo**

La forma tiene un cuadro de límite de ajuste de texto que es 5 unidades más grande que la ruta de acceso.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 