---
title: Atributo AlbumIDAlbumArtist
description: El atributo AlbumIDAlbumArtist es un identificador único para el álbum.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- AlbumIDAlbumArtist Media Player de Windows
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700077"
---
# <a name="albumidalbumartist-attribute"></a>Atributo AlbumIDAlbumArtist

El atributo **AlbumIDAlbumArtist** es un identificador único para el álbum.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en la biblioteca.

El identificador único es una combinación del título del álbum y el nombre del intérprete del álbum. En este atributo, el nombre del intérprete del álbum aparece primero. Cuando se usa el método [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obtener un objeto **StringCollection** mediante este atributo, los valores se ordenan por nombre de intérprete del álbum.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





