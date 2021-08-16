---
title: Atributo LibraryID
description: El atributo LibraryID es el identificador de la biblioteca a la que pertenece el elemento.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Atributo LibraryID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a011db4e18509761c232bcf5439e33445128ef77c50945f84662a7b7956f607f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468225"
---
# <a name="libraryid-attribute"></a>Atributo LibraryID

El **atributo LibraryID** es el identificador de la biblioteca a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Un elemento multimedia podría pertenecer a la biblioteca local del usuario actual o pertenecer a una biblioteca que otro usuario haya puesto a disposición de otro usuario en la red principal o en Internet.

El valor de este atributo es el mismo que el valor devuelto por el [**método IWMPLibrary2::getItemInfo.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





