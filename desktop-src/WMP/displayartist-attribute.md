---
title: Atributo DisplayArtist
description: El atributo DisplayArtist es el nombre del intérprete que se muestra para un elemento.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- DisplayArtist Attribute Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c20e3d693aa7d5be5be0236d9eefebe7efcb70bc236db3f84389e5a3ceeccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997325"
---
# <a name="displayartist-attribute"></a>Atributo DisplayArtist

El **atributo DisplayArtist** es el nombre del intérprete que se muestra para un elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Comentarios

Por lo general, **DisplayArtist** tendrá el mismo valor que el atributo **WM/AlbumArtist** cuando se establezca ese atributo. De lo contrario, el valor será el nombre del intérprete que está asociado a la primera pista del álbum.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Atributo WM/AlbumArtist**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





