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
ms.openlocfilehash: ce3e3d2948419761a139139493e737df1a9a709147613eadd3e077f0f5101f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332635"
---
# <a name="wmalbumcoverurl-attribute"></a>Atributo WM/AlbumCoverURL

El **atributo WM/AlbumCoverURL es** el localizador uniforme de recursos (URL) para el arte del álbum o una imagen en miniatura.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Para un elemento de audio, este atributo es la dirección URL del arte del álbum. Para un elemento de foto o vídeo, este atributo es la dirección URL de una imagen en miniatura.

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para elementos multimedia que pertenecen a una biblioteca remota; es decir, una biblioteca que otro usuario ha puesto a disposición de los usuarios en la red doméstica. Para determinar si una biblioteca multimedia es remota, llame al [**tipo IWMPLibrary::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





