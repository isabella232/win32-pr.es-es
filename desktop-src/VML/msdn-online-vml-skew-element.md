---
title: Elemento SKEW de VML
description: Elemento SKEW de VML
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099045"
---
# <a name="vml-skew-element"></a>Elemento SKEW de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un sesgo para una forma.

Los atributos siguientes modifican un sesgo.



| Atributo                                 | Descripción                                    |
|-------------------------------------------|------------------------------------------------|
| [Ext](ext-attribute--skew--vml.md)       | Define la forma en que se muestra un sesgo.           |
| [Id](id-attribute--skew--vml.md)         | Define un identificador único para un sesgo.        |
| [Matriz](matrix-attribute--skew--vml.md) | Define una transformación de perspectiva para un sesgo.    |
| [Offset](offset-attribute--skew--vml.md) | Define el desplazamiento de un sesgo.                  |
| [Activado](on-attribute--skew--vml.md)         | Determina si se mostrará el sesgo. |
| [Origen](origin-attribute--skew--vml.md) | Determina el origen de un sesgo.               |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

Además, los [atributos Matrix](matrix-attribute--skew--vml.md) y [On](on-attribute--skew--vml.md) deben establecerse en **True.**

A continuación se muestra el código mínimo necesario para generar un sesgo.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



El **elemento Skew** es una extensión Microsoft Office a VML.

**Ejemplos**

-   [Ejemplo de asimetría simple](/previous-versions/bb229482(v=vs.85))
-   [Ejemplo de asimetría dinámica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 