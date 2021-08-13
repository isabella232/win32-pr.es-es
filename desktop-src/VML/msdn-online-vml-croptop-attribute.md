---
title: Atributo CropTop de VML
description: Atributo CropTop de VML
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c66351941c789216eb484ee2a25c090d95df0d2c67a60133bbe7ac4cab44a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601512"
---
# <a name="vml-croptop-attribute"></a>Atributo CropTop de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el porcentaje de eliminación de imágenes del lado superior. Lectura/escritura **Numbernumber .**

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* croptop=" *expression* ">

**Sintaxis de script**

*element* .croptop="*expression*"

*expresión* = *elemento*.croptop

**Comentarios:**

La cantidad de recorte puede oscilar entre -1,0 y 1,0. El valor predeterminado es 0. Tenga en cuenta que un valor de 1 no mostrará ninguna imagen. Los valores negativos darán lugar a que la imagen se atrase hacia dentro desde el borde que se recorta (el espacio vacío entre la imagen y el borde recortado se rellenará con el color de relleno de la forma). Los valores positivos menores que 1 darán lugar a que la imagen restante se ajuste a la forma.

*Atributo estándar de VML*

**Ejemplo**

La imagen se exprimirá en una lonja estrecha en la parte inferior de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 