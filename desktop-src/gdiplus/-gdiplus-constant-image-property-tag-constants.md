---
description: Varios formatos de archivo de imagen permiten almacenar metadatos junto con una imagen.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de etiquetas de propiedades de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509caf20659628909d225bb2dc34a4dbaa27047c08e361b28e9777141f213751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696423"
---
# <a name="image-property-tag-constants"></a>Constantes de etiquetas de propiedades de imagen

Varios formatos de archivo de imagen permiten almacenar metadatos junto con una imagen. Los metadatos son información sobre una imagen, por ejemplo, el título, el ancho, el modelo de cámara y el intérprete. Windows GDI+ proporciona una manera uniforme de almacenar y recuperar metadatos de archivos de imagen en los formatos Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) y Exchangeable Image File (EXIF).

En GDI+, un fragmento de metadatos se denomina elemento de propiedad *y* un elemento de propiedad individual se identifica mediante una constante numérica denominada etiqueta *de propiedad*. Puede almacenar y recuperar metadatos llamando a los métodos [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) de la clase [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y no tiene que preocuparse por los detalles de cómo un formato de archivo determinado almacena los metadatos.

Los temas siguientes enumeran y describen los elementos de propiedad admitidos por GDI+. Las descripciones son breves y generales para que se apliquen a una variedad de formatos de archivo. Para obtener una descripción detallada de cómo se usa un elemento de propiedad en un formato de archivo determinado, consulte la especificación de ese formato de archivo. Para obtener vínculos a varias especificaciones de formato de archivo, vea [Especificaciones de formato de archivo de imagen.](-gdiplus-constant-image-file-format-specifications.md) Para obtener más información sobre los [**metadatos,**](-gdiplus-constant-image-property-tag-type-constants.md)vea Leer y [escribir metadatos](-gdiplus-reading-and-writing-metadata-use.md) y Constantes de tipo de etiqueta de propiedad de imagen.

-   [Etiquetas de propiedad en orden numérico](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Etiquetas de propiedad en orden alfabético](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descripciones de elementos de propiedad](-gdiplus-constant-property-item-descriptions.md)

 

 



