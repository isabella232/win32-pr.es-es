---
title: Elemento sesgado de VML
description: Elemento sesgado de VML
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e317d03fc0bbef361df56282bec55ea2a9e708f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487739"
---
# <a name="vml-skew-element"></a>Elemento sesgado de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un sesgo para una forma.

Los atributos siguientes modifican un sesgo.



| Atributo                                 | Descripción                                    |
|-------------------------------------------|------------------------------------------------|
| [Total](ext-attribute--skew--vml.md)       | Define la forma en que se muestra un sesgo.           |
| [Id](id-attribute--skew--vml.md)         | Define un identificador único para un sesgo.        |
| [Matriz](matrix-attribute--skew--vml.md) | Define una transformación de perspectiva para un sesgo.    |
| [Offset](offset-attribute--skew--vml.md) | Define el desplazamiento de un sesgo.                  |
| [Activado](on-attribute--skew--vml.md)         | Determina si se mostrará el sesgo. |
| [Origen](origin-attribute--skew--vml.md) | Determina el origen de un sesgo.               |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

Además, la [matriz](matrix-attribute--skew--vml.md) [y los](on-attribute--skew--vml.md) atributos deben establecerse en **true**.

A continuación se encuentra el código mínimo necesario para producir un sesgo.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



El elemento **skew** es una extensión Microsoft Office a VML.

**Ejemplos**

-   [Ejemplo de sesgo simple](/previous-versions/bb229482(v=vs.85))
-   [Ejemplo de sesgo dinámico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 