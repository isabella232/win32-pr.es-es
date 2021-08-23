---
title: Atributo copyright (Msfeeds.h)
description: El atributo Copyright es el mensaje de copyright del elemento.
ms.assetid: 617272cb-883f-46d6-b0a9-29ac32c63148
keywords:
- Copyright Attribute Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Copyright
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b42e68e0d3485824f502dea991048121e788dfbe574b8fa4921e93a3b7afb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651965"
---
# <a name="copyright-attribute"></a>Atributo copyright

El **atributo Copyright** es el mensaje de copyright del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Archivos multimedia de Windows usados con frecuencia](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMCopyright.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                    |
| Header<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





