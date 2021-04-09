---
title: Atributo Position (relleno) (VML)
description: Atributo Position (relleno) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149588"
---
# <a name="position-attribute-fillvml"></a>Atributo Position (relleno) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la posición de la imagen de relleno. Lectura/escritura [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* position = " *expresión* " >

**Sintaxis de script**

*Element* . position = "*expresión*"

*expresión* = de *elemento*. Position

**Comentarios:**

Especifica un punto de la forma para colocar el origen de la imagen. El valor predeterminado es el centro del rectángulo del contenedor. El vector es una fracción del ancho y el alto de la imagen.

*Atributo estándar de VML*

**Ejemplo**

La imagen del relleno se desplaza hacia la derecha hasta un punto 50% del ancho de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 