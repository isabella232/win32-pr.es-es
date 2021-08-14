---
title: Atributo EndCap de VML
description: Atributo EndCap de VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b2d36eb76b840ca8f89aebf3dadefaa68093394a07bd78db0e8fa0b18ed555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346720"
---
# <a name="vml-endcap-attribute"></a>Atributo EndCap de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el estilo de extremo para el final de un trazo. Lectura/escritura **DvLineEndCapStyle**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* endcap=" *expression* ">

**Sintaxis de script**

*element* .endcap="*expression*"

*expresión* = *elemento*.endcap

**Comentarios:**

Estos valores incluyen:

-   Plano (valor predeterminado)
-   Square
-   Round

*Atributo estándar de VML*

**Ejemplo**

Se dibuja una línea con un extremo plano al final del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 