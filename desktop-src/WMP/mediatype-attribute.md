---
title: MediaType (atributo)
description: El atributo MediaType es el tipo de contenido del elemento.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Atributo MediaType Media Player Windows
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653545"
---
# <a name="mediatype-attribute"></a>MediaType (atributo)

El atributo **mediatype** es el tipo de contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotografía](photo-item-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en la biblioteca.

Este atributo tiene uno de los valores siguientes: "audio", "otro", "foto", "lista de reproducción", "radio" o "vídeo". Use este atributo con el *MediaCollection*. método **getByAttribute** para recuperar una lista de reproducción que contenga todos los elementos de un tipo determinado.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**MediaCollection.getByAttribute**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





