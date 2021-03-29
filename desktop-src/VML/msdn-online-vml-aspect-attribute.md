---
title: Atributo de aspecto VML
description: Atributo de aspecto VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792400"
---
# <a name="vml-aspect-attribute"></a>Atributo de aspecto VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica cómo se conservará la relación de aspecto de la imagen de relleno. Lectura/escritura **Cadena**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* Aspect = " *expresión* " >

**Sintaxis de script**

*Element* . Aspect = "*expresión*"

*expresión* = de *elemento*. Aspect

**Comentarios:**

Estos valores incluyen:



| Value   | Descripción                           |
|---------|---------------------------------------|
| ignore  | Omitir problemas de aspecto. Predeterminada.        |
| al menos | La imagen es al menos tan grande como **el tamaño**. |
| Atmos  | La imagen no es más grande que **el tamaño**.     |



 

*Atributo estándar de VML*

**Ejemplo**

La imagen que constituye el relleno es mayor o igual que un tamaño de 10 puntos en 10 puntos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 