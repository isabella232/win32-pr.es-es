---
title: Atributo StartArrowWidth de VML
description: Atributo StartArrowWidth de VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513245"
---
# <a name="vml-startarrowwidth-attribute"></a>Atributo StartArrowWidth de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el ancho de la punta de flecha para el inicio de una línea. Lectura/escritura **DvArrowheadWidth**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* startarrowwidth=" *expression* ">

**Sintaxis de script**

*Element* .startarrowwidth="*expression*"

*expresión* = *elemento*.startarrowwidth

**Comentarios:**

Estos valores incluyen:

-   Estrecho
-   Media (valor predeterminado)
-   Ancho

Atributo estándar de VML

**Ejemplo**

Se dibuja una línea con una punta de flecha clásica ancha al principio del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 