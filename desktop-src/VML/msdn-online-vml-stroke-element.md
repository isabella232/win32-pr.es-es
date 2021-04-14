---
title: Elemento de trazo de VML
description: Elemento de trazo de VML
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62048227fca074276b825ceedb793eaa9a5d84dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487858"
---
# <a name="vml-stroke-element"></a>Elemento de trazo de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un trazo para una forma.

Los atributos siguientes modifican un trazo.



| Atributo                                                          | Descripción                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [AltHRef](althref-attribute--stroke--vml.md)                      | Especifica una referencia alternativa para un trazo.                |
| [Color](color-attribute--stroke--vml.md)                          | Define el color de un trazo.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Define un segundo color para un trazo.                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | Especifica el patrón de puntos y guiones de un trazo.              |
| [EndArrow](msdn-online-vml-endarrow-attribute.md)                 | Define un estilo de punta de flecha para el final de un trazo.           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | Define una longitud de la punta de flecha para el final de un trazo.          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | Define un ancho de la punta de flecha para el final de un trazo.           |
| [EndCap](msdn-online-vml-endcap-attribute.md)                     | Define el estilo de extremo para el final de un trazo.                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | Define el tipo de relleno utilizado para el fondo de un trazo. |
| [Referencia](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Define la dirección URL de la imagen original del trazo.         |
| [Id](id-attribute--stroke--vml.md)                                | Define un identificador único para el trazo.                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | Determina la alineación de una imagen de trazo.                   |
| [ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | Define cómo se conservará la relación de aspecto de la imagen del trazo.  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | Define el tamaño de la imagen del trazo.                 |
| [JoinStyle](msdn-online-vml-joinstyle-attribute.md)               | Define el estilo de combinación de una polilínea.                         |
| [Estilo de línea](msdn-online-vml-linestyle-attribute.md)               | Define el estilo de línea de un trazo.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Define la suavidad de una unión angular.                      |
| [Activado](on-attribute--stroke--vml.md)                                | Determina si se mostrará el trazo.              |
| [Opacidad](opacity-attribute--stroke--vml.md)                      | Define la cantidad de transparencia de un trazo.               |
| [Diez](src-attribute--stroke--vml.md)                              | Define la imagen de origen que se va a cargar para un relleno de trazo.           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | Define la punta de flecha para el inicio de un trazo.              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | Define la longitud de la punta de flecha para el inicio de un trazo.       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | Define el ancho de la punta de flecha para el inicio de un trazo.        |
| [Título](title-attribute--stroke--vml.md)                          | Define el título de un trazo.                                |
| [Peso](msdn-online-vml-weight-attribute.md)                     | Define el grosor de un trazo.                            |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

En el código siguiente se muestra cómo se puede usar el elemento **Stroke** para modificar una línea.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**Ejemplos**

-   [Ejemplo de trazo simple](/previous-versions/bb229466(v=vs.85))
-   [Ejemplo de imagen de trazo](/previous-versions/bb229468(v=vs.85))

 

 