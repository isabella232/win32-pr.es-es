---
title: Atributo ID (imagen) (VML)
description: Atributo ID (imagen) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421371"
---
# <a name="id-attribute-imagevml"></a>Atributo ID (imagen) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un nombre que proporciona un identificador único para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: ID. de *elemento* = " *expresión* " >

**Sintaxis de script**

*Element* . ID = "*expresión*"

*expresión* = de identificador de *elemento*

**Comentarios:**

Use el **identificador** para hacer referencia a una imagen específica. Una vez que haya creado una imagen y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular la imagen.

**Atributo estándar de VML**

**Ejemplo**

La forma tiene un identificador de **ImageData** denominado "mi imagen".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 