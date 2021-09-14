---
title: Atributo MediaType
description: El atributo MediaType es el tipo de contenido del elemento.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Atributo MediaType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361735"
---
# <a name="mediatype-attribute"></a>Atributo MediaType

El **atributo MediaType** es el tipo de contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotos](photo-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en la biblioteca.

Este atributo tiene uno de los siguientes valores: "audio", "other", "photo", "playlist", "radio" o "video". Use este atributo con *MediaCollection*. **Método getByAttribute** para recuperar una lista de reproducción que contiene todos los elementos de un tipo determinado.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**MediaCollection.getByAttribute**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





