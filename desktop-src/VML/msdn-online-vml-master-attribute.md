---
title: Atributo maestro de VML
description: Atributo maestro de VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d126b9d02144bbc8831d7be9e73a3e5896c2ceccca71cfcbc8161d5ccc8112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999115"
---
# <a name="vml-master-attribute"></a>Atributo maestro de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si un **elemento ShapeType** es un elemento maestro. Lectura/escritura **DvTriState**.

**Se aplica a**

[ShapeType](msdn-online-vml-shapetype-element.md)

**Sintaxis de etiquetas**

<v: *element* o:master=" *expression* ">

**Comentarios:**

Si **es True**, el motor de representación representa la forma **ShapeType.** El valor predeterminado es **False**.

*Microsoft Office Atributo Extensions*

**Ejemplo**

El **elemento ShapeType** es una forma maestra.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 