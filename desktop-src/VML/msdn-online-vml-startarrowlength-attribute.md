---
title: Atributo StartArrowLength de VML
description: Atributo StartArrowLength de VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25446737118c546727d769d54d98e4503faaadd063102fa98a417ebea13c976d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395835"
---
# <a name="vml-startarrowlength-attribute"></a>Atributo StartArrowLength de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la longitud de la punta de flecha para el inicio de una línea. Lectura/escritura **DvArrowheadLength**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* startarrowlength=" *expression* ">

**Sintaxis de script**

*Element* .startarrowlength="*expression*"

*expresión* = *elemento*.startarrowlength

**Comentarios:**

Estos valores incluyen:

-   Short
-   Media (valor predeterminado)
-   long

Atributo estándar de VML

**Ejemplo**

Se dibuja una línea con una punta de flecha clásica corta al principio del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 