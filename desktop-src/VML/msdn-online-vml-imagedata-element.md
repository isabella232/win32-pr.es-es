---
title: Elemento ImageData de VML
description: Elemento ImageData de VML
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b416a53f97efc8a1f1875eda0e842c4cfbe96bf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676407"
---
# <a name="vml-imagedata-element"></a>Elemento ImageData de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una imagen para una forma.

Los atributos siguientes modifican una imagen.



| Atributo                                                          | Descripción                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Especifica una referencia alternativa para una imagen.                        |
| [Suavizado](msdn-online-vml-bilevel-attribute.md)                   | Determina si una imagen se mostrará en blanco y negro.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Determina la intensidad de negro en una imagen.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Define el color del palatte que se tratará como transparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Define el porcentaje de eliminación de imágenes del lado inferior.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Define el porcentaje de eliminación de imágenes del lado izquierdo.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Define el porcentaje de eliminación de imágenes del lado derecho.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Define el porcentaje de eliminación de imágenes del lado superior.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Determina si se detectará un clic del mouse.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Define el color de los efectos de color en relieve.                         |
| [Beneficios](msdn-online-vml-gain-attribute.md)                         | Define la intensidad de todos los colores de una imagen.                      |
| [Gamma](msdn-online-vml-gamma-attribute.md)                       | Define la cantidad de contraste de una imagen.                          |
| [Aclarar](msdn-online-vml-grayscale-attribute.md)               | Determina si una imagen se mostrará en el modo de escala de grises.          |
| [Referencia](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Define una dirección URL para una imagen.                                           |
| [Id](id-attribute--image--vml.md)                                 | Define un identificador único para una imagen.                             |
| [Película](msdn-online-vml-movie-attribute.md)                       | Define un puntero a una imagen de película.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Almacena el identificador OLE de una imagen.                                        |
| [Diez](src-attribute--imagedata--vml.md)                           | Define un origen para la imagen.                                       |
| [Título](title-attribute--imagedata--vml.md)                       | Define el título de una imagen.                                        |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

Además, el atributo [**src**](src-attribute--imagedata--vml.md) debe apuntar a una imagen.

A continuación se encuentra el código mínimo necesario para generar una imagen.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> En versiones preliminares de VML, este elemento se llamaba **imagen** .

 

**Ejemplos**

-   [Ejemplo de ImageData simple](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Ejemplo de ImageData dinámico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 