---
title: On Attribute (Stroke)(VML)
description: On Attribute (Stroke)(VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5682200a44a98d2b4c074b11db172e2b94b812a196a404927a33b4d142289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007575"
---
# <a name="on-attribute-strokevml"></a>On Attribute (Stroke)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará el trazo. Lectura/escritura **DvTriState**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* on=" *expression* ">

**Sintaxis de script**

*element* .on="*expression*"

*expresión* = *elemento*.on

**Comentarios:**

Si **es False**, no se muestra el trazo. El valor predeterminado es **True**.

*Atributo estándar de VML*

**Ejemplo**

No se mostrará el trazo.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 