---
title: Atributo WM/AlbumCoverURL
description: El atributo WM/AlbumCoverURL es el localizador uniforme de recursos (URL) para el arte del álbum o una imagen en miniatura.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Atributo WM/AlbumCoverURL Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466423"
---
# <a name="wmalbumcoverurl-attribute"></a>Atributo WM/AlbumCoverURL

El **atributo WM/AlbumCoverURL es** el localizador uniforme de recursos (URL) para el arte del álbum o una imagen en miniatura.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Para un elemento de audio, este atributo es la dirección URL de la imagen del álbum. Para un elemento de foto o vídeo, este atributo es la dirección URL de una imagen en miniatura.

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para elementos multimedia que pertenecen a una biblioteca remota; es decir, una biblioteca que otro usuario ha puesto a disposición de los usuarios en la red principal. Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary::get \_ escriba**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





