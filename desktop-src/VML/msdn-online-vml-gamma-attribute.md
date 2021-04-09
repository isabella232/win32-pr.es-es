---
title: Atributo gamma de VML
description: Atributo gamma de VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149441"
---
# <a name="vml-gamma-attribute"></a>Atributo gamma de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la cantidad de contraste de una imagen. Lectura/escritura **VgNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *elemento* gamma = " *expresión* " >

**Sintaxis de script**

*Element* . gamma = "*expresión*"

*expresión* = de *Element*. gamma

**Comentarios:**

Al reducir el valor gamma inferior a 1 se modifica una imagen para que sea más contrastada, mientras que los valores mayores que 1 disminuyen el contraste. Los valores útiles son de 0,3 a aproximadamente 3. El valor predeterminado es 0.

*Atributo estándar de VML*

**Ejemplo**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 