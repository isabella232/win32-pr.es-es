---
title: Atributo VmL Dekey
description: Atributo VmL Dekey
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d279f31ff4910ceb121242f587aac88585dba2cfc8278320c0d86680f4f330b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999315"
---
# <a name="vml-chromakey-attribute"></a>Atributo VmL Dekey

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el valor de color de la imagen que se tratará como transparente. Lectura/escritura **DvColor**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* element elementkey=" *expression* ">

**Sintaxis de script**

*element* .elementkey="*expression*"

*expresión* = *element*.element .element

**Comentarios:**

Use este atributo para que las partes de una imagen se transparenten mediante la clave de la transparencia en un color específico. Por ejemplo, si hace que el valor **Dekey** sea **negro,** cualquier parte de la imagen que sea negra será transparente y el color de relleno "mostrará" esa parte de la imagen.

*Atributo estándar de VML*

**Ejemplo**

Las áreas de la imagen que son de color negro sólido se volverán transparentes, lo que permitirá que el color de relleno verde se muestre a través de esas áreas en su lugar.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 