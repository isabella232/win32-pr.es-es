---
title: Atributo CropBottom de VML
description: Atributo CropBottom de VML
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667e5501f43d55dcc6a489406e4b10397c1a39773fad2fce7dc6f8601bf45024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601958"
---
# <a name="vml-cropbottom-attribute"></a>Atributo CropBottom de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el porcentaje de eliminación de imágenes del lado inferior. Lectura/escritura **Numbernumber .**

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* cropbottom=" *expression* ">

**Sintaxis de script**

*element* .cropbottom="*expression*"

*expresión* = *elemento*.cropbottom

**Comentarios:**

La cantidad de recorte puede oscilar entre -1,0 y 1,0. El valor predeterminado es 0. Tenga en cuenta que un valor de 1 no mostrará ninguna imagen. Los valores negativos darán lugar a que la imagen se atrase hacia dentro desde el borde que se recorta (el espacio vacío entre la imagen y el borde recortado se rellenará con el color de relleno de la forma). Los valores positivos menores que 1 darán lugar a que la imagen restante se ajuste a la forma.

Atributo estándar de VML

**Ejemplo**

No se mostrará ninguna imagen porque la imagen está recortada al 100 % desde la parte inferior.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 