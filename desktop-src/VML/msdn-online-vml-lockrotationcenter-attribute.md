---
title: Atributo LockRotationCenter de VML
description: Atributo LockRotationCenter de VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676477"
---
# <a name="vml-lockrotationcenter-attribute"></a>Atributo LockRotationCenter de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si el atributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) especifica el giro del objeto extruido. Lectura/escritura **VgTriState**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* lockrotationcenter = " *expresión* " >

**Sintaxis de script**

*Element* . lockrotationcenter = "*expresión*"

*expresión* = de *elemento*. lockrotationcenter

**Comentarios:**

Si es **false**, el atributo de [orientación](msdn-online-vml-orientation-attribute.md) especifica el giro. El valor predeterminado es **True**.

Observe lo siguiente:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



es igual que:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office atributo Extensions*

 

 