---
title: Atributo WM/AlbumArtist
description: El atributo WM/AlbumArtist es el nombre del intérprete principal del álbum.
ms.assetid: 9da02a85-d0cf-41e3-ad5b-08b908315993
keywords:
- Atributo WM/AlbumArtist Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/AlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550805894ed3744400afe0e118834b437908f173447139b2c3ebad15391288a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761445"
---
# <a name="wmalbumartist-attribute"></a>Atributo WM/AlbumArtist

El **atributo WM/AlbumArtist** es el nombre del intérprete principal del álbum.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**AlbumArtist** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMAlbumArtist.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





