---
title: Objeto MetadataPicture
description: El objeto MetadataPicture proporciona una manera de recuperar los valores del atributo de metadatos de WM/imagen. Este atributo corresponde a la carátula de álbum contenida en un archivo multimedia digital, no a la carátula de álbum descargada a través de Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Objeto MetadataPicture Media Player de Windows
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488130"
---
# <a name="metadatapicture-object"></a>Objeto MetadataPicture

El objeto **MetadataPicture** proporciona una manera de recuperar los valores del atributo de metadatos de [**WM/imagen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) . Este atributo corresponde a la carátula de álbum contenida en un archivo multimedia digital, no a la carátula de álbum descargada a través de Internet.

El objeto **MetadataPicture** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**denominación**](metadatapicture-description.md) | Recupera una descripción de la imagen de metadatos.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Recupera el tipo MIME de la imagen de metadatos.    |
| [**Tal**](metadatapicture-picturetype.md) | Recupera el tipo de imagen de la imagen de metadatos. |
| [**URL**](metadatapicture-url.md)                 | Exclusivamente para uso interno.                                |



 

Se tiene acceso al objeto **MetadataPicture** mediante el método siguiente.



| Object                        | Método                                               |
|-------------------------------|------------------------------------------------------|
| [**Medios**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

`player.currentMedia.getItemInfoByType(name, language, index)`En lo que respecta a la ilustración, se usa en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 