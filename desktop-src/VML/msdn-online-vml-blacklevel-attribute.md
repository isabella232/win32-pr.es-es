---
title: Atributo BlackLevel de VML
description: Atributo BlackLevel de VML
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077963"
---
# <a name="vml-blacklevel-attribute"></a>Atributo BlackLevel de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la intensidad de negro en una imagen. Lectura/escritura **VgNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *Element* blacklevel = " *expresión* " >

**Sintaxis de script**

*Element* . blacklevel = "*expresión*"

*expresión* = de *elemento*. blacklevel

**Comentarios:**

Permite que el nivel de color se modifique para que los negros aparezcan como verdaderos negros y todos los demás colores estén visibles como sombras por encima del negro. El valor predeterminado es 0. Aunque se permite cualquier número entre infinitos positivos y negativos, los valores menores que-0,5 se mostrarán como todos los negros y los valores superiores a 0,5 se mostrarán como todos los blancos.

*Atributo estándar de VML*

**Ejemplo**

La imagen se mostrará con tonos muy oscuros.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 