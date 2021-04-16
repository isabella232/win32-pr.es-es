---
title: Atributo DisplayArtist
description: El atributo DisplayArtist es el nombre del artista que se muestra para un elemento.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- DisplayArtist Media Player de Windows
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699624"
---
# <a name="displayartist-attribute"></a>Atributo DisplayArtist

El atributo **DisplayArtist** es el nombre del artista que se muestra para un elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Observaciones

Por lo general, **DisplayArtist** tendrá el mismo valor que el atributo **WM/AlbumArtist** cuando se establezca ese atributo. De lo contrario, el valor será el nombre del artista asociado a la primera pista del álbum.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Atributo WM/AlbumArtist**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





