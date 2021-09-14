---
title: Atributo AlbumIDAlbumArtist
description: El atributo AlbumIDAlbumArtist es un identificador único del álbum.
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
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890121"
---
# <a name="albumidalbumartist-attribute"></a>Atributo AlbumIDAlbumArtist

El **atributo AlbumIDAlbumArtist** es un identificador único del álbum.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en la biblioteca.

El identificador único es una combinación del título del álbum y el nombre del intérprete del álbum. En este atributo, el nombre del intérprete del álbum es el primero. Cuando se usa el [método MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obtener un objeto **StringCollection** con este atributo, los valores se ordenan por el nombre del intérprete del álbum.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





