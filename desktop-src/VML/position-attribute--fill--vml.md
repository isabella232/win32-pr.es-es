---
title: Atributo Position (Fill)(VML)
description: Atributo Position (Fill)(VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5db5742238fbf1ede0ab3777944d1f67dd7e3787674515177b299af1ab3a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844869"
---
# <a name="position-attribute-fillvml"></a>Atributo Position (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la posición de la imagen de relleno. Lectura/escritura [DvVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* position=" *expression* ">

**Sintaxis de script**

*element* .position="*expression*"

*expresión* = *elemento*.position

**Comentarios:**

Especifica un punto de la forma para colocar el origen de la imagen. El valor predeterminado es el centro del rectángulo del contenedor. El vector es una fracción del ancho y alto de la imagen.

*Atributo estándar de VML*

**Ejemplo**

La imagen del relleno se desplaza a la derecha hasta un punto del 50 % del ancho de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 