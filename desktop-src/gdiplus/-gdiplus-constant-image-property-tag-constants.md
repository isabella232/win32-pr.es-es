---
description: Varios formatos de archivo de imagen permiten almacenar metadatos junto con una imagen.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de etiqueta de propiedad de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985203"
---
# <a name="image-property-tag-constants"></a>Constantes de etiqueta de propiedad de imagen

Varios formatos de archivo de imagen permiten almacenar metadatos junto con una imagen. Los metadatos son información acerca de una imagen, como el título, el ancho, el modelo de cámara y el artista. Windows GDI+ proporciona una manera uniforme de almacenar y recuperar metadatos de archivos de imagen en los formatos de Tagged Image File Format (TIFF), JPEG, gráficos de red portátiles (PNG) y de archivo de imagen intercambiable (EXIF).

En GDI+, una parte de los metadatos se denomina *elemento de propiedad* y un elemento de propiedad individual se identifica mediante una constante numérica denominada etiqueta de *propiedad*. Puede almacenar y recuperar los metadatos mediante una llamada a los métodos [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) de la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , y no tiene que preocuparse por los detalles de cómo un formato de archivo determinado almacena esos metadatos.

En los temas siguientes se enumeran y describen los elementos de propiedad admitidos por GDI+. Las descripciones son breves y generales para que se apliquen a una variedad de formatos de archivo. Para obtener una descripción detallada de cómo se usa un elemento de propiedad en un formato de archivo determinado, vea la especificación de ese formato de archivo. Para obtener vínculos a varias especificaciones de formato de archivo, consulte [Especificaciones de formato de archivo de imagen](-gdiplus-constant-image-file-format-specifications.md). Para obtener más información sobre los metadatos, vea [lectura y escritura de metadatos](-gdiplus-reading-and-writing-metadata-use.md) y [**constantes de tipo de etiqueta de propiedad de imagen**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Etiquetas de propiedad en orden numérico](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Etiquetas de propiedad en orden alfabético](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descripciones de elementos de propiedad](-gdiplus-constant-property-item-descriptions.md)

 

 



