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
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068451"
---
# <a name="displayartist-attribute"></a>Atributo DisplayArtist

El **atributo DisplayArtist** es el nombre del intérprete que se muestra para un elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Observaciones

Por lo general, **DisplayArtist** tendrá el mismo valor que el **atributo WM/AlbumArtist** cuando se establezca ese atributo. De lo contrario, el valor será el nombre del intérprete que está asociado con la primera pista del álbum.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Version<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Atributo WM/AlbumArtist**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





