---
title: Atributo WM/AlbumArtist
description: El atributo WM/AlbumArtist es el nombre del intérprete principal del álbum.
ms.assetid: 9da02a85-d0cf-41e3-ad5b-08b908315993
keywords:
- Media Player de Windows de atributos de WM/AlbumArtist
topic_type:
- apiref
api_name:
- WM/AlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61c7f50c377468dd7cb58a2be8a63fd3df6a201
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708747"
---
# <a name="wmalbumartist-attribute"></a>Atributo WM/AlbumArtist

El atributo **WM/AlbumArtist** es el nombre del intérprete principal del álbum.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**AlbumArtist** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMAlbumArtist.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





