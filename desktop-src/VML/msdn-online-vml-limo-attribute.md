---
title: Atributo limo de VML
description: Atributo limo de VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420777"
---
# <a name="vml-limo-attribute"></a>Atributo limo de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un punto de estiramiento en la ruta de acceso. Lectura/escritura **Vector2D**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *Element* limo = " *expresión* " >

**Sintaxis de script**

*Element* . limo = "*expresión*"

*expresión* = de *elemento*. limo

**Comentarios:**

El valor predeterminado es "0 0". Limo stretchs son puntos en el borde de una forma que definen dónde y cómo un usuario puede ajustar una forma en un editor gráfico.

*Atributo estándar de VML*

**Ejemplo**

Un punto de estiramiento de limo se define A la mitad de la línea horizontal.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 