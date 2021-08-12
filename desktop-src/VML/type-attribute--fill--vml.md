---
title: Atributo type (Fill)(VML)
description: Atributo type (Fill)(VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883318c82758178ee9693a1199cb76c5798e351ec809aecb54fe7d0a266d85d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596146"
---
# <a name="type-attribute-fillvml"></a>Atributo type (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina el tipo de relleno. Lectura/escritura **FillFillType**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* type=" *expression* ">

**Sintaxis de script**

*element* .type="*expression*"

*expresión* = *element*.type

**Comentarios:**

Estos valores incluyen:



| Tipo           | Descripción                                                             |
|----------------|-------------------------------------------------------------------------|
| Sólido          | El patrón de relleno es sólido. Predeterminada.                                     |
| degradados       | Los colores de relleno se combinan en un degradado lineal de abajo a arriba. |
| gradientradial | Los colores de relleno se combinan en un degradado radial.                    |
| tile           | La imagen de relleno está en mosaico.                                                |
| pattern        | La imagen se usa para crear un patrón con los colores de relleno.            |
| frame          | La imagen se extiende para rellenar la forma.                               |



 

**Atributo estándar de VML**

**Ejemplo**

Se crea un primer plano rojo y un relleno de fondo azul mediante el patrón de la imagen myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 