---
title: Atributo type (Fill) (VML)
description: Atributo type (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792754"
---
# <a name="type-attribute-fillvml"></a>Atributo type (Fill) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina el tipo de relleno. Lectura/escritura **VgFillType**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* Type = " *expresión* " >

**Sintaxis de script**

*Element* . Type = "*expresión*"

*expresión* = de *elemento*. Type

**Comentarios:**

Estos valores incluyen:



| Tipo           | Descripción                                                             |
|----------------|-------------------------------------------------------------------------|
| barra          | El patrón de relleno es sólido. Predeterminada.                                     |
| degradados       | Los colores de relleno se combinan en un degradado lineal de abajo a arriba. |
| gradientradial | Los colores de relleno se combinan en un degradado radial.                    |
| tile           | La imagen de relleno está en mosaico.                                                |
| pattern        | La imagen se usa para crear un patrón con los colores de relleno.            |
| frame          | La imagen se ajusta para rellenar la forma.                               |



 

**Atributo estándar de VML**

**Ejemplo**

Se crea un relleno de fondo rojo y de primer plano azul mediante el patrón de la imagen myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 