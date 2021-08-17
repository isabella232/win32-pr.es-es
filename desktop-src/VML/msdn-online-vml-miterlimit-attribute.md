---
title: Atributo MiterLimit de VML
description: Atributo MiterLimit de VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef82ce7e8e0d3bf99fc532a9e746a94006a6bb9deba282ce8edd6ab91d41902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308375"
---
# <a name="vml-miterlimit-attribute"></a>Atributo MiterLimit de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la subilidad de la unión de los mitros. Lectura/escritura **Numbernumber .**

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *elemento* miterlimit=" *expresión* ">

**Sintaxis de script**

*Element* .miterlimit="*expression*"

*expresión* = *elemento*.miterlimit

**Comentarios:**

Distancia máxima entre el punto interno y el punto exterior de una unión. Este número es un múltiplo del grosor de la línea.

El valor predeterminado es 8.

*Atributo estándar de VML*

**Ejemplo**

Las uniones de la polilínea se mitraen con un límite de 10, es decir, 5 veces 2 puntos.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 