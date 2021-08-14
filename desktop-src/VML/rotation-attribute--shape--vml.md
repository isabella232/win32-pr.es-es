---
title: Atributo Rotation (Shape)(VML)
description: Atributo Rotation (Shape)(VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f73b55b57a7b9d9d7f14cdae4ec71a38a1e38246a4430339db23f35a339430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754140"
---
# <a name="rotation-attribute-shapevml"></a>Atributo Rotation (Shape)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el ángulo en el que se gira una forma. Lectura/escritura [DvangleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="rotation: *expression* ">

**Sintaxis de script**

*element* .rotation="*expression*"

*expresión* = *elemento*.rotation

**Comentarios:**

El valor en grados puede ser positivo o negativo, y los valores mayores de 360 se modularizan a un círculo de 360 grados. Los ángulos positivos son en el sentido de las agujas del reloj. El valor predeterminado es 0.

Tenga en cuenta que la forma se cambia de posición después de la rotación para reflejar las nuevas coordenadas del cuadro de límite.

Tenga en cuenta también que para el scripting, no se usa el atributo **de** estilo y que **Rotation** se trata como un atributo directo de la forma.

El **atributo Rotation** es similar al atributo de rotación HTML estándar para los estilos. 

*Atributo estándar de VML*

**Vea también**

**Ejemplo**

El rectángulo se inclinará 45 grados.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Ejemplo de atributo de rotación](/previous-versions/bb264091(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 