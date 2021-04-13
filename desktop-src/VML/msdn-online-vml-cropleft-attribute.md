---
title: Atributo CropLeft de VML
description: Atributo CropLeft de VML
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271279"
---
# <a name="vml-cropleft-attribute"></a>Atributo CropLeft de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el porcentaje de eliminación de imágenes del lado izquierdo. Lectura/escritura **VgNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *elemento* CropLeft = " *expresión* " >

**Sintaxis de script**

*Element* . CropLeft = "*expresión*"

*expresión* = de *elemento*. CropLeft

**Comentarios:**

La cantidad de recorte puede oscilar entre-1,0 y 1,0. El valor predeterminado es 0. Tenga en cuenta que el valor 1 no mostrará ninguna imagen. Los valores negativos provocarán que la imagen se apriete hacia adentro desde el borde que se va a recortar (el color de relleno de la forma se rellenará con el espacio vacío entre la imagen y el borde recortado). Los valores positivos inferiores a 1 darán lugar a que la imagen restante se estire para ajustarse a la forma.

*Atributo estándar de VML*

**Ejemplo**

el 20% de la imagen se quitará en el lado izquierdo y la imagen restante se ajustará para ajustarse a la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 