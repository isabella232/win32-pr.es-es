---
title: Atributo AlignShape de VML
description: Atributo AlignShape de VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359362"
---
# <a name="vml-alignshape-attribute"></a>Atributo AlignShape de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si una imagen se alineará con una forma. Lectura/escritura **VgTriState**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* alignshape = " *expresión* " >

**Sintaxis de script**

*Element* . alignshape = "*expresión*"

*expresión* = de *elemento*. alignshape

**Comentarios:**

Si es **true**, la imagen utilizada para crear el relleno está alineada con la forma. Si es **false**, la imagen utilizada para crear el relleno está alineada con la ventana. El valor predeterminado es **true**.

*Atributo estándar de VML*

**Ejemplo**

La imagen de relleno en mosaico creada a partir de myimage.gif se alinea con la ventana, no con la forma; Aunque la forma se gira, la imagen no lo es.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 