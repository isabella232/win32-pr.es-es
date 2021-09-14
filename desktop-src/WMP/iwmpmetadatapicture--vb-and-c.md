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
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361737"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interfaz IWMPMetadataPicture (VB y C#)

Proporciona propiedades para obtener información sobre la imagen contenida en un archivo multimedia digital representado por un [**atributo de metadatos WM/Picture.**](/windows/desktop/wmformat/wmpicture) Este atributo corresponde a las imágenes de arte del álbum contenidas en un archivo multimedia digital, no al arte del álbum descargado a través de Internet.

La **interfaz IWMPMetadataPicture** expone las siguientes propiedades.



| Propiedad.                                                                                   | Descripción                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Descripción**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Obtiene la descripción de la imagen representada por el atributo de metadatos.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Obtiene el tipo MIME de la imagen representada por el atributo de metadatos.    |
| [**pictureType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Obtiene el tipo de imagen de la imagen representada por el atributo de metadatos. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Exclusivamente para uso interno.                                                        |



 

Obtenga una **interfaz IWMPMetadataPicture** pasando el nombre de atributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) al método siguiente y conversión del objeto que se devuelve.



| Interfaz                                  | Propiedad.                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Members

La **interfaz IWMPMetadataPicture (VB y C#)** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

