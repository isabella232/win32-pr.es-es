---
title: Atributo AlignShape de VML
description: Atributo AlignShape de VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00e1fe8d07fb04c198ced2e2eb50d6ef0e6c020984d2d8cf12a3ca37cf09d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125318"
---
# <a name="vml-alignshape-attribute"></a>Atributo AlignShape de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si una imagen se alineará con una forma. Lectura/escritura **DvTriState**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* alignshape=" *expression* ">

**Sintaxis de script**

*element* .alignshape="*expression*"

*expresión* = *elemento*.alignshape

**Comentarios:**

Si **es True**, la imagen utilizada para crear el relleno se alinea con la forma . Si **es False,** la imagen utilizada para crear el relleno se alinea con la ventana. El valor predeterminado es **true**.

*Atributo estándar de VML*

**Ejemplo**

La imagen de relleno en mosaico creada myimage.gif se alinea con la ventana, no con la forma; aunque la forma se gira, la imagen no lo es.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 