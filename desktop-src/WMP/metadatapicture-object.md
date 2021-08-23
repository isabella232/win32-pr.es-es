---
title: MetadataPicture (objeto)
description: El objeto MetadataPicture proporciona una manera de recuperar los valores del atributo de metadatos WM/Picture. Este atributo corresponde al arte del álbum contenido en un archivo multimedia digital, no al arte del álbum descargado a través de Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- MetadataPicture Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996215"
---
# <a name="metadatapicture-object"></a>MetadataPicture (objeto)

El **objeto MetadataPicture** proporciona una manera de recuperar los valores del atributo [**de metadatos WM/Picture.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) Este atributo corresponde al arte del álbum contenido en un archivo multimedia digital, no al arte del álbum descargado a través de Internet.

El **objeto MetadataPicture** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**Descripción**](metadatapicture-description.md) | Recupera una descripción de la imagen de metadatos.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Recupera el tipo MIME de la imagen de metadatos.    |
| [**pictureType**](metadatapicture-picturetype.md) | Recupera el tipo de imagen de la imagen de metadatos. |
| [**URL**](metadatapicture-url.md)                 | Exclusivamente para uso interno.                                |



 

Se **tiene acceso al objeto MetadataPicture** mediante el método siguiente.



| Object                        | Método                                               |
|-------------------------------|------------------------------------------------------|
| [**Medios**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

Para fines ilustrativos, `player.currentMedia.getItemInfoByType(name, language, index)` se usa en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 