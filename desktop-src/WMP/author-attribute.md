---
title: Atributo Author
description: El atributo Author es el nombre de un actor o intérprete multimedia asociado al contenido.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Atributo Author Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f7bd6acf39142f3947a4df623b4ce2450f3a872386f1f68ec8d7e600b831f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864885"
---
# <a name="author-attribute"></a>Atributo Author

El **atributo Author** es el nombre de un actor o intérprete multimedia asociado al contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Archivos multimedia de Windows usados habitualmente](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Media.getItemInfoByType](media-getiteminfobytype.md)
-   [Elementos de fotos](photo-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar *media*. **Método getItemInfoByType,** no *media*. **Método getItemInfo.**

La Windows SDK de formato multimedia para este atributo es g \_ wszWMAuthor.

**Actor** y **Artist** son alias de este atributo.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





