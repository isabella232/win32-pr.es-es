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
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889868"
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

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar *media*. **Método getItemInfoByType,** no *media*. **Método getItemInfo.**

La Windows SDK de formato multimedia para este atributo es g \_ wszWMAuthor.

**Actor** y **Artist** son alias de este atributo.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





