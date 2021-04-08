---
title: Elemento de sombra VML
description: Elemento de sombra VML
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995294"
---
# <a name="vml-shadow-element"></a>Elemento de sombra VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una sombra para una forma.

Los atributos siguientes modifican una sombra.



| Atributo                                          | Descripción                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Color](color-attribute--shadow--vml.md)          | Define el color de una sombra.                     |
| [Color2](color2-attribute--shadow--vml.md)        | Define el segundo color de una sombra.              |
| [Id](id-attribute--shadow--vml.md)                | Especifica el identificador único de una sombra.       |
| [Matriz](matrix-attribute--shadow--vml.md)        | Define la transformación de perspectiva de una sombra.     |
| [Oculta](msdn-online-vml-obscured-attribute.md) | Determina si la sombra es transparente.      |
| [Offset](offset-attribute--shadow--vml.md)        | Define hasta qué punto se extiende la sombra más allá de la forma. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Define un segundo desplazamiento.                           |
| [Activado](on-attribute--shadow--vml.md)                | Determina si se muestra una sombra.          |
| [Opacidad](opacity-attribute--shadow--vml.md)      | Determina la transparencia de una sombra.           |
| [Origen](origin-attribute--shadow--vml.md)        | Define el centro de la sombra.                  |
| [Tipo](type-attribute--shadow--vml.md)            | Especifica el tipo de sombra.                      |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

Además, el atributo [on](on-attribute--shadow--vml.md) debe establecerse en **true**.

A continuación se encuentra el código mínimo necesario para producir una sombra.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



Es posible que no advierta la sombra a menos que aumente los valores de [desplazamiento](offset-attribute--shadow--vml.md) , ya que el desplazamiento predeterminado es 2PT, 2PT.

**Ejemplos**

-   [Ejemplo de sombra simple](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Ejemplo de sombra dinámica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 