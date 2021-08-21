---
title: Atributo AlternateSourceURL
description: El atributo AlternateSourceURL es un localizador uniforme de recursos para el elemento multimedia que actúa como alternativa a los atributos DLNASourceURI y SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Atributo AlternateSourceURL Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055243"
---
# <a name="alternatesourceurl-attribute"></a>Atributo AlternateSourceURL

El **atributo AlternateSourceURL** es un localizador uniforme de recursos para el elemento multimedia que actúa como alternativa a los atributos [**DLNASourceURI**](dlnasourceuri-attribute.md) y [**SourceURL.**](sourceurl-attribute.md)

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para elementos multimedia que pertenecen a una biblioteca remota; es decir, una biblioteca que otro usuario ha puesto a disposición de los usuarios en la red principal. Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary::get \_ escriba**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





