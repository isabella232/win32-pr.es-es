---
title: Atributo WM/ProviderRating
description: El atributo WM/ProviderRating es la clasificación del elemento asignado por el proveedor de los valores de atributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Atributo WM/ProviderRating Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcff262f21b4f31daff6f704dba1cb096f54bb295a21a3ae9a7c90f574af34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116618"
---
# <a name="wmproviderrating-attribute"></a>Atributo WM/ProviderRating

El **atributo WM/ProviderRating** es la clasificación del elemento asignado por el proveedor de los valores de atributo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**La** clasificación es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMProviderRating.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





