---
title: Atributo WM/Genre
description: El atributo WM/Genre es el género del contenido.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Atributo WM/Genre Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0ef67b0b41ff59f644b0d52376428ae7a2330d388aa62f9765cb4842eeb561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000985"
---
# <a name="wmgenre-attribute"></a>Atributo WM/Genre

El **atributo WM/Genre** es el género del contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar el método **Media.getItemInfoByType,** no el **método Media.getItemInfo.**

**Genre** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMGenre.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





