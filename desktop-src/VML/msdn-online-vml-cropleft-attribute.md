---
title: Atributo CropLeft de VML
description: Atributo CropLeft de VML
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26112aa969e95c6bfb1ec715024aca9eb17b2dbfc2d7d214fb3679cf7ab77447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754855"
---
# <a name="vml-cropleft-attribute"></a>Atributo CropLeft de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el porcentaje de eliminación de imágenes del lado izquierdo. Lectura/escritura **NumberNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* cropleft=" *expression* ">

**Sintaxis de script**

*element* .cropleft="*expression*"

*expresión* = *elemento*.cropleft

**Comentarios:**

La cantidad de recorte puede oscilar entre -1,0 y 1,0. El valor predeterminado es 0. Tenga en cuenta que un valor de 1 no mostrará ninguna imagen. Los valores negativos darán lugar a que la imagen se atrase hacia dentro desde el borde recortada (el espacio vacío entre la imagen y el borde recortado se rellenará con el color de relleno de la forma). Los valores positivos menores que 1 darán lugar a que la imagen restante se ajuste a la forma.

*Atributo estándar de VML*

**Ejemplo**

El 20 % de la imagen se quitará en el lado izquierdo y la imagen restante se ajustará para ajustarse a la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 