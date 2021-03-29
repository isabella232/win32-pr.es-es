---
title: Atributo WrapCoords de VML
description: Atributo WrapCoords de VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792123"
---
# <a name="vml-wrapcoords-attribute"></a>Atributo WrapCoords de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el polígono delimitador que rodea una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* o:wrapcoords = " *expresión* " >

**Comentarios:**

Describe una lista delimitada por comas de x y ycoordinates; es decir, "x1, Y1, x2, Y2, x3, Y3,..." Se usa cuando el texto se ajusta estrechamente alrededor de una forma. El valor predeterminado es **null** (una cadena vacía) hasta que el atributo **MSO-Wrap-Mode** esté establecido en **tight** o **a través** de.

*Microsoft Office atributo Extensions*

**Ejemplo**

La forma tiene un cuadro de límite de ajuste de texto que es 5 unidades mayor que la ruta de acceso.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 