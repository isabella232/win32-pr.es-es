---
title: Interfaz IWMPMetadataPicture (VB y C) (WMP. h)
description: Proporciona propiedades para obtener información sobre la imagen contenida en un archivo multimedia digital representado por un atributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB y C) interfaz de Windows Media Player
- IWMPMetadataPicture (VB y C) interfaz de Windows Media Player, se describe
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690770"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interfaz IWMPMetadataPicture (VB y C#)

Proporciona propiedades para obtener información acerca de la imagen contenida en un archivo multimedia digital representado por un atributo de metadatos de [**WM/imagen**](/windows/desktop/wmformat/wmpicture). Este atributo corresponde a las imágenes de carátulas de álbum contenidas en un archivo multimedia digital, no a la carátula de álbum descargada a través de Internet.

La interfaz **IWMPMetadataPicture** expone las siguientes propiedades.



| Propiedad                                                                                   | Descripción                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Descripción**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Obtiene la descripción de la imagen representada por el atributo de metadatos.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Obtiene el tipo MIME de la imagen representada por el atributo de metadatos.    |
| [**Tal**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Obtiene el tipo de imagen de la imagen representada por el atributo de metadatos. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Exclusivamente para uso interno.                                                        |



 

Obtenga una interfaz **IWMPMetadataPicture** pasando el nombre de atributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) al método siguiente y convirtiendo el objeto que se devuelve.



| Interfaz                                  | Propiedad                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Miembros

La interfaz **IWMPMetadataPicture (VB y C#)** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

