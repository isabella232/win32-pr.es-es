---
title: Atributo AlbumID
description: El atributo AlbumID es un identificador único para el álbum.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Atributo AlbumID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2690e4b6dd6bf6c8d795c8a06aca9c65c3f2c17513cf9b8ab8d55419b00d517
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124075"
---
# <a name="albumid-attribute"></a>Atributo AlbumID

El **atributo AlbumID** es un identificador único para el álbum.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo solo se almacena en la biblioteca.

El identificador único es una combinación del título del álbum y el nombre del intérprete del álbum. En este atributo, el título del álbum es el primero. Cuando se usa el [método MediaCollection.getAttributeStringCollection para](mediacollection-getattributestringcollection.md) obtener un **objeto StringCollection** con este atributo, los valores se ordenan por título del álbum.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributo AlbumIDAlbumArtist**](albumidalbumartist-attribute.md)
</dt> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





