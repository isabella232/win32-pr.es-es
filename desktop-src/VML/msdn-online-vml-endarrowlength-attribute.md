---
title: Atributo EndArrowLength de VML
description: Atributo EndArrowLength de VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb11c07300127acd2446c7c2c643e0a891957d63f7650044514427f3e8535d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601355"
---
# <a name="vml-endarrowlength-attribute"></a>Atributo EndArrowLength de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una longitud de punta de flecha para el final de una línea. Lectura/escritura **DvArrowheadLength**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* endarrowlength=" *expression* ">

**Sintaxis de script**

*Element* .endarrowlength="*expression*"

*expresión* = *elemento*.endarrowlength

**Comentarios:**

Estos valores incluyen:

-   Short
-   Media (valor predeterminado)
-   long

*Atributo estándar de VML*

**Ejemplo**

Se dibuja una línea con una punta de flecha clásica corta al final del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 