---
title: Elemento Imagedata de VML
description: Elemento Imagedata de VML
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3a307dd36daf0ff08d2fab7cd9086a3bc07447872cf36cb41972e4aa5a4d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600296"
---
# <a name="vml-imagedata-element"></a>Elemento Imagedata de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una imagen para una forma.

Los atributos siguientes modifican una imagen.



| Atributo                                                          | Descripción                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Especifica una referencia alternativa para una imagen.                        |
| [Binivel](msdn-online-vml-bilevel-attribute.md)                   | Determina si una imagen se mostrará en blanco y negro.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Determina la intensidad del negro en una imagen.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Define el color de la paleta que se tratará como transparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Define el porcentaje de eliminación de imágenes del lado inferior.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Define el porcentaje de eliminación de imágenes del lado izquierdo.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Define el porcentaje de eliminación de imágenes del lado derecho.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Define el porcentaje de eliminación de imágenes del lado superior.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Determina si se detectará un clic del mouse.                    |
| [RelievessColor](msdn-online-vml-embosscolor-attribute.md)           | Define el color de los efectos de color con relieve.                         |
| [Ganar](msdn-online-vml-gain-attribute.md)                         | Define la intensidad de todos los colores de una imagen.                      |
| [Gamma](msdn-online-vml-gamma-attribute.md)                       | Define la cantidad de contraste de una imagen.                          |
| [Grises](msdn-online-vml-grayscale-attribute.md)               | Determina si una imagen se mostrará en modo de escala de grises.          |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Define una dirección URL para una imagen.                                           |
| [Id](id-attribute--image--vml.md)                                 | Define un identificador único para una imagen.                             |
| [Película](msdn-online-vml-movie-attribute.md)                       | Define un puntero a una imagen de película.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Almacena el identificador OLE de una imagen.                                        |
| [Fuente](src-attribute--imagedata--vml.md)                           | Define un origen para la imagen.                                       |
| [Título](title-attribute--imagedata--vml.md)                       | Define el título de una imagen.                                        |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

Además, el [**atributo Src**](src-attribute--imagedata--vml.md) debe apuntar a una imagen.

A continuación se muestra el código mínimo necesario para generar una imagen.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> En las versiones anteriores de VML, este elemento se llamaba **Image** .

 

**Ejemplos**

-   [Ejemplo de ImageData simple](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Ejemplo de Dynamic ImageData](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 