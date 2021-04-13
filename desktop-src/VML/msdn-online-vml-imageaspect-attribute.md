---
title: Atributo ImageAspect de VML
description: Atributo ImageAspect de VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359134"
---
# <a name="vml-imageaspect-attribute"></a>Atributo ImageAspect de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define cómo se conservará la relación de aspecto de la imagen del trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v:

Element *imageaspect = "* expresión *" >*

**Sintaxis de script**

Element *. imageaspect = "* expresión *"*

*=* elemento Expression *. imageaspect*

**Comentarios:**

Estos valores incluyen:



| Value   | Descripción                                |
|---------|--------------------------------------------|
| Ignorar  | Omitir problemas de aspecto.                      |
| Al menos | La imagen es al menos tan grande como **ImageSize**. |
| AtMos  | La imagen no es mayor que **ImageSize**.     |



 

En cada caso, el atributo **ImageSize** se ajustará para conservar el aspecto de la imagen.

*Atributo estándar de VML*

**Ejemplo**

La imagen del trazo será al menos tan grande como el tamaño de la imagen.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 