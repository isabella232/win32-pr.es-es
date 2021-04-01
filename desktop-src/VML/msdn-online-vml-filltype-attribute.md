---
title: Atributo FillType de VML
description: Atributo FillType de VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995606"
---
# <a name="vml-filltype-attribute"></a>Atributo FillType de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el tipo de relleno utilizado para el fondo de un trazo. Lectura/escritura **VgFillType**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* filltype = " *expresión* " >

**Sintaxis de script**

*Element* . filltype = "*expresión*"

*expresión* = de *elemento*. filltype

**Comentarios:**

Estos valores incluyen:



| DashStyle | Descripción                                    |
|-----------|------------------------------------------------|
| Sólido     | El patrón de relleno es sólido. Valor predeterminado.      |
| Tile      | La imagen de relleno está en mosaico.                       |
| Patrón   | La imagen de relleno se ajusta para formar un patrón. |
| Fotograma     | La imagen de relleno se convierte en un borde para la forma. |



 

*Atributo estándar de VML*

**Ejemplo**

El trazo de la forma tiene una textura en mosaico creada a partir de la imagen de cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 