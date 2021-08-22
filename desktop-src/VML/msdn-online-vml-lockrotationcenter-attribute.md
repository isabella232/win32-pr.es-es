---
title: Atributo LockRotationCenter de VML
description: Atributo LockRotationCenter de VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0cfee24998cfa343265569274ace688a05f90a270b721317394e59589a51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598063"
---
# <a name="vml-lockrotationcenter-attribute"></a>Atributo LockRotationCenter de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si el atributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) especifica la rotación del objeto extruido. Lectura/escritura **DvTriState**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* lockrotationcenter=" *expression* ">

**Sintaxis de script**

*element* .lockrotationcenter="*expression*"

*expresión* = *elemento*.lockrotationcenter

**Comentarios:**

Si **es False**, el atributo Orientation especifica la [rotación.](msdn-online-vml-orientation-attribute.md) El valor predeterminado es **True**.

Tenga en cuenta que:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



es igual que:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Atributo Extensions*

 

 