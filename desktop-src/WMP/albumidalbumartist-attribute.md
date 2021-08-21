---
title: Atributo AlbumIDAlbumArtist
description: El atributo AlbumIDAlbumArtist es un identificador único para el álbum.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Atributo AlbumIDAlbumArtist Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4905f0448c7e08abe308a57b1ad08020d47563847db1aa32744c0de3279cdcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055393"
---
# <a name="albumidalbumartist-attribute"></a>Atributo AlbumIDAlbumArtist

El **atributo AlbumIDAlbumArtist** es un identificador único para el álbum.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo solo se almacena en la biblioteca.

El identificador único es una combinación del título del álbum y el nombre del intérprete del álbum. En este atributo, el nombre del intérprete del álbum es el primero. Cuando se usa el [método MediaCollection.getAttributeStringCollection para](mediacollection-getattributestringcollection.md) obtener un objeto **StringCollection** con este atributo, los valores se ordenan por el nombre del intérprete del álbum.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





