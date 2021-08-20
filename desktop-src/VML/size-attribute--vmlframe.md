---
title: Atributo Size (VMLFrame)
description: Atributo Size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754130"
---
# <a name="size-attribute-vmlframe"></a>Atributo Size (VMLFrame)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tamaño de la región de recorte del marco. Lectura/escritura **DvVector2D**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *element* size=" *expression* ">

**Sintaxis de script**

*element* .size="*expression*"

*expresión* = *elemento*.size

**Comentarios:**

El valor predeterminado es 0,0. Tenga en **cuenta que Tamaño** solo funciona si [Clip](msdn-online-vml-clip-attribute.md) es **True.** En este atributo, el tamaño se define como el ancho y alto del marco.

*Atributo estándar de VML*

**Ejemplo**

El tamaño de la región de recorte será de 50pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 