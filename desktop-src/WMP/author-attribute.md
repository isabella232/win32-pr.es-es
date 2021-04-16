---
title: Atributo Author
description: El atributo Author es el nombre de un intérprete o actor multimedia asociado con el contenido.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Media Player de atributos de autor de Windows
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699890"
---
# <a name="author-attribute"></a>Atributo Author

El atributo **Author** es el nombre de un intérprete o actor multimedia asociado con el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Archivos de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Media. getItemInfoByType](media-getiteminfobytype.md)
-   [Elementos de fotografía](photo-item-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe utilizar los *medios*. método **getItemInfoByType** , no el *medio*. método **getItemInfo** .

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMAuthor.

**Actor** y **intérprete** son alias para este atributo.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





