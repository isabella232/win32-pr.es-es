---
title: Atributo ImageAspect de VML
description: Atributo ImageAspect de VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f67d715d5cd10d36b4e8e7e32f939aeeef2bbdd894aba9da5a069ef03f0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600358"
---
# <a name="vml-imageaspect-attribute"></a>Atributo ImageAspect de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define cómo se conservará la relación de aspecto de la imagen de trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v:

element *imageaspect="* expression *">*

**Sintaxis de script**

element *.imageaspect="* expression *"*

elemento *=* *de expresión .imageaspect*

**Comentarios:**

Estos valores incluyen:



| Value   | Descripción                                |
|---------|--------------------------------------------|
| Ignore  | Omitir problemas de aspecto.                      |
| Atleast | Image es al menos tan grande como **ImageSize.** |
| Atmost  | Image no es mayor que **ImageSize.**     |



 

En cada caso, el **atributo ImageSize** se ajustará para conservar el aspecto de la imagen.

*Atributo estándar de VML*

**Ejemplo**

La imagen de trazo será al menos tan grande como el tamaño de la imagen.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 