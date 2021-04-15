---
title: Atributo WM/AlbumCoverURL
description: El atributo WM/AlbumCoverURL es el localizador uniforme de recursos (URL) para carátulas de álbum o una imagen en miniatura.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Media Player de Windows de atributos de WM/AlbumCoverURL
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708743"
---
# <a name="wmalbumcoverurl-attribute"></a>Atributo WM/AlbumCoverURL

El atributo **WM/AlbumCoverURL** es el localizador uniforme de recursos (URL) para carátulas de álbum o una imagen en miniatura.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotografía**](photo-item-attributes.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Para un elemento de audio, este atributo es la dirección URL de la carátula del álbum. Para un elemento de foto o vídeo, este atributo es la dirección URL de una imagen en miniatura.

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica. Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Windows Media Player 12 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





