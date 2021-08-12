---
title: Atributo de aspecto de VML
description: Atributo de aspecto de VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669b0f93e740e6bc4d4fb94155f6ca0ab60d5e00cebfb1604d5272d45d4dd8ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602902"
---
# <a name="vml-aspect-attribute"></a>Atributo de aspecto de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica cómo se conservará la relación de aspecto de la imagen de relleno. Lectura/escritura **Cadena**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* aspect=" *expression* ">

**Sintaxis de script**

*element* .aspect="*expression*"

*expresión* = *elemento*.aspect

**Comentarios:**

Estos valores incluyen:



| Value   | Descripción                           |
|---------|---------------------------------------|
| ignore  | Omitir problemas de aspecto. Predeterminada.        |
| Atleast | La imagen es al menos tan grande como **Size**. |
| Atmost  | La imagen no es mayor que **Size**.     |



 

*Atributo estándar de VML*

**Ejemplo**

La imagen que forma el relleno es mayor o igual que un tamaño de 10 puntos por 10 puntos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 