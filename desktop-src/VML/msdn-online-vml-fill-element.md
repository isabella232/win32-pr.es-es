---
title: Elemento de relleno de VML
description: Elemento de relleno de VML
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc7205baa9db0eaa7d84d4022057f81804ea790
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995607"
---
# <a name="vml-fill-element"></a>Elemento de relleno de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un relleno para una forma.

Los atributos siguientes modifican un relleno.



| Atributo                                                          | Descripción                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [AlignShape](msdn-online-vml-alignshape-attribute.md)             | Determina si una imagen se alineará con una forma.   |
| [AltHRef](althref-attribute--fill--vml.md)                        | Especifica una referencia alternativa para una imagen.         |
| [Angulo](angle-attribute--fill--vml.md)                            | Define el ángulo de un relleno de degradado.                  |
| [Aspecto](msdn-online-vml-aspect-attribute.md)                     | Especifica cómo se conservará el aspecto del relleno de la imagen. |
| [Color](color-attribute--fill--vml.md)                            | Define el color de un relleno.                           |
| [Color2](color2-attribute--fill--vml.md)                          | Define el segundo color de un relleno.                   |
| [Colores](msdn-online-vml-colors-attribute.md)                     | Define varios colores para un relleno de degradado.           |
| [DetectMouseClick](detectmouseclick-attribute--fill--vml.md)      | Determina si se detecta un clic del mouse.          |
| [Foco](msdn-online-vml-focus-attribute.md)                       | Define el centro de un relleno de degradado lineal.          |
| [FocusPosition](msdn-online-vml-focusposition-attribute.md)       | Define el centro de un relleno de degradado radial.          |
| [FocusSize](msdn-online-vml-focussize-attribute.md)               | Define el tamaño del foco para un relleno radial.              |
| [Referencia](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Define una dirección URL para el archivo de imagen original.              |
| [Id](id-attribute--fill--vml.md)                                  | Define un identificador único para el relleno.              |
| [Método](msdn-online-vml-method-attribute.md)                     | Define el método utilizado para generar un relleno de degradado.   |
| [Activado](on-attribute--fill--vml.md)                                  | Determina si se muestra el relleno.          |
| [Opacidad](opacity-attribute--fill--vml.md)                        | Define la transparencia de un relleno.                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | Define la transparencia del segundo color de relleno.     |
| [Origen](origin-attribute--fill--vml.md)                          | Define el centro de una imagen.                        |
| [Position](position-attribute--fill--vml.md)                      | Define la posición de una imagen.                      |
| [Tamaño](size-attribute--fill--vml.md)                              | Define el tamaño de una imagen.                          |
| [Diez](src-attribute--fill--vml.md)                                | Define la imagen que se va a cargar para un relleno.                  |
| [Título](title-attribute--fill--vml.md)                            | Define el título de un relleno.                           |
| [Tipo](type-attribute--fill--vml.md)                              | Define el tipo de relleno.                              |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

En el código siguiente se muestra un relleno de degradado simple para una forma.


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**Ejemplos**

-   [Relleno de degradado simple](/previous-versions/bb229620(v=vs.85))
-   [Ejemplo de relleno dinámico](/previous-versions/bb229621(v=vs.85))

 

 