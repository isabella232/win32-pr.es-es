---
title: Atributo CropRight de VML
description: Atributo CropRight de VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d695bb3fd9e88c3357343860dcbbff820e5a49a22100d59fe46c502b642e31d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796305"
---
# <a name="vml-cropright-attribute"></a>Atributo CropRight de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el porcentaje de eliminación de imágenes del lado derecho. Lectura/escritura **NumberNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* cropright=" *expression* ">

**Sintaxis de script**

*element* .cropright="*expression*"

*expresión* = *elemento*.cropright

**Comentarios:**

La cantidad de recorte puede oscilar entre -1,0 y 1,0. El valor predeterminado es 0. Tenga en cuenta que un valor de 1 no mostrará ninguna imagen. Los valores negativos darán lugar a que la imagen se atrase hacia dentro desde el borde recortada (el espacio vacío entre la imagen y el borde recortado se rellenará con el color de relleno de la forma). Los valores positivos menores que 1 darán lugar a que la imagen restante se ajuste a la forma.

*Atributo estándar de VML*

**Ejemplo**

La imagen se exprimirá desde el lado derecho en un 20 % del ancho. El espacio vacío entre la imagen y el borde derecho se rellenará con el color de relleno de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 