---
title: Atributo de escala de grises VML
description: Atributo de escala de grises VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420926"
---
# <a name="vml-grayscale-attribute"></a>Atributo de escala de grises VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si una imagen se mostrará en el modo de escala de grises. Lectura/escritura **VgTriState**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *elemento* de escala de grises = " *expresión* " >

**Sintaxis de script**

*Element* . = "*expresión*"

*expresión* = de *elemento*. escala de grises

**Comentarios:**

Si **es true**, la imagen se mostrará en escala de grises en lugar de en color. El valor predeterminado es **False**.

El valor se basa en la recomendación de CCIR 709, que favorece un mayor peso verde y produce resultados más agradables para el color natural.

*Atributo estándar de VML*

**Ejemplo**

La imagen se mostrará en escala de grises en lugar de en color.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 