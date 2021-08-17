---
title: Interfaz IWMPMetadataPicture (VB y C) (Wmp.h)
description: Proporciona propiedades para obtener información sobre la imagen contenida en un archivo multimedia digital representado por un atributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- Interfaz IWMPMetadataPicture (VB y C) Reproductor de Windows Media
- Interfaz IWMPMetadataPicture (VB y C) Reproductor de Windows Media , descrito
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b73a48b2ea93d696f2b8780edec90dfcf0522e2353c508e31d96dd7a404d0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996495"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interfaz IWMPMetadataPicture (VB y C#)

Proporciona propiedades para obtener información sobre la imagen contenida en un archivo multimedia digital representado por un [**atributo de metadatos WM/Picture.**](/windows/desktop/wmformat/wmpicture) Este atributo corresponde a las imágenes de arte del álbum contenidas en un archivo multimedia digital, no a las imágenes de álbum descargadas a través de Internet.

La **interfaz IWMPMetadataPicture** expone las siguientes propiedades.



| Propiedad                                                                                   | Descripción                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Descripción**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Obtiene la descripción de la imagen representada por el atributo de metadatos.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Obtiene el tipo MIME de la imagen representada por el atributo de metadatos.    |
| [**pictureType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Obtiene el tipo de imagen de la imagen representada por el atributo de metadatos. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Exclusivamente para uso interno.                                                        |



 

Obtenga una **interfaz IWMPMetadataPicture** pasando el nombre de atributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) al método siguiente y conversión del objeto que se devuelve.



| Interfaz                                  | Propiedad                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Miembros

La **interfaz IWMPMetadataPicture (VB y C#)** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

