---
title: Atributo EndArrow de VML
description: Atributo EndArrow de VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f289342c8bfb67e9a0c2ccc6e418f42bd954e9826a18f07260a2891bf4b4284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007835"
---
# <a name="vml-endarrow-attribute"></a>Atributo EndArrow de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una punta de flecha para el final de una línea. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* endarrow=" *expression* ">

**Sintaxis de script**

*Element* .endarrow="*expression*"

*expresión* = *elemento*.endarrow

**Comentarios:**

Estos valores incluyen:

-   Ninguna (valor predeterminado)
-   Bloquear
-   Clásico
-   Diamond
-   Elipse
-   Abrir

*Atributo estándar de VML*

**Ejemplo**

Se dibuja una línea con una punta de flecha clásica al final del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 