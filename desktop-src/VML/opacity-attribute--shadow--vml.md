---
title: Atributo de opacidad (sombra) (VML)
description: Atributo de opacidad (sombra) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420846"
---
# <a name="opacity-attribute-shadowvml"></a>Atributo de opacidad (sombra) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina la transparencia de una sombra. Lectura/escritura [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *elemento* Opacity = " *expresión* " >

**Sintaxis de script**

*elemento* . Opacity = "*expresión*"

*expresión* = de *elemento*. Opacity

**Comentarios:**

El valor predeterminado es 1. Un valor de 0 hará una sombra completamente transparente.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene una sombra que es 50% transparente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 