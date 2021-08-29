---
title: Atributo StartArrow de VML
description: Atributo StartArrow de VML
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b0d1ce8d352ef119e2745d0f7768332ad074d134877b03433aa788f1bb2e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754487"
---
# <a name="vml-startarrow-attribute"></a>Atributo StartArrow de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la punta de flecha para el inicio de una línea. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* startarrow=" *expression* ">

**Sintaxis de script**

*element* .startarrow="*expression*"

*expresión* = *elemento*.startarrow

**Comentarios:**

Estos valores incluyen:

-   Ninguna (valor predeterminado)
-   Bloquear
-   Clásico
-   Diamond
-   Elipse
-   Abrir

Atributo estándar de VML

**Ejemplo**

Se dibuja una línea con una punta de flecha clásica al principio del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 