---
title: Elemento Shadow de VML
description: Elemento Shadow de VML
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55440f47da0fb5b9b70c94c7df66cef941af5746c924a3a72cc5081ddbe627e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099115"
---
# <a name="vml-shadow-element"></a>Elemento Shadow de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una sombra para una forma.

Los atributos siguientes modifican una sombra.



| Atributo                                          | Descripción                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Color](color-attribute--shadow--vml.md)          | Define el color de una sombra.                     |
| [Color2](color2-attribute--shadow--vml.md)        | Define el segundo color de una sombra.              |
| [Id](id-attribute--shadow--vml.md)                | Especifica el identificador único de una sombra.       |
| [Matriz](matrix-attribute--shadow--vml.md)        | Define la transformación de perspectiva de una sombra.     |
| [Oscurecido](msdn-online-vml-obscured-attribute.md) | Determina si la sombra es transparente.      |
| [Offset](offset-attribute--shadow--vml.md)        | Define hasta qué punto la sombra se extiende más allá de la forma. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Define un segundo desplazamiento.                           |
| [Activado](on-attribute--shadow--vml.md)                | Determina si se muestra una sombra.          |
| [Opacidad](opacity-attribute--shadow--vml.md)      | Determina la transparencia de una sombra.           |
| [Origen](origin-attribute--shadow--vml.md)        | Define el centro de la sombra.                  |
| [Tipo](type-attribute--shadow--vml.md)            | Especifica el tipo de sombra.                      |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

Además, el [atributo On](on-attribute--shadow--vml.md) debe establecerse en **True.**

A continuación se muestra el código mínimo necesario para generar una sombra.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



Es posible que no observe la sombra a menos que aumente los [valores de Desplazamiento,](offset-attribute--shadow--vml.md) ya que el desplazamiento predeterminado es 2pt,2pt.

**Ejemplos**

-   [Ejemplo de sombra simple](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Ejemplo de sombra dinámica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 