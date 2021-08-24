---
title: Atributo Origin (VMLFrame)(VML)
description: Atributo Origin (VMLFrame)(VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874b857a2408927e296f82f0f9aa0a5e15f6da69b1e2af6eaf6ebe2c5df746d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768265"
---
# <a name="origin-attribute-vmlframevml"></a>Atributo Origin (VMLFrame)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el origen de la región de recorte del marco. Lectura/escritura **DvVector2D**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *element* origin=" *expression* ">

**Sintaxis de script**

*element* .origin="*expression*"

*expresión* = *elemento*.origin

**Comentarios:**

El valor predeterminado es 0,0. Tenga en **cuenta que Origin** solo funciona si [Clip](msdn-online-vml-clip-attribute.md) es **True.** En este atributo, el origen se define como la esquina superior izquierda del marco.

*Atributo estándar de VML*

**Ejemplo**

El origen de la región de recorte es 100pt,100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 