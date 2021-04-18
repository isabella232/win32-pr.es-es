---
title: Atributo MediaContentTypes
description: El atributo MediaContentTypes especifica el tipo de contenido del elemento.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- MediaContentTypes Media Player de Windows
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653546"
---
# <a name="mediacontenttypes-attribute"></a>Atributo MediaContentTypes

El atributo **MediaContentTypes** especifica el tipo de contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Reproducción](playlist-attributes-ref.md)

## <a name="remarks"></a>Observaciones

Este atributo puede ser uno de los siguientes valores:



| Value | Significado                                |
|-------|----------------------------------------|
| 1     | La lista de reproducción contiene contenido de audio.   |
| 2     | Que se va a proporcionar.                        |
| 3     | La lista de reproducción contiene contenido de audio.   |
| 4     | La lista de reproducción contiene contenido de vídeo.   |
| 5     | La lista de reproducción contiene el contenido de la imagen. |
| 6     | La lista de reproducción contiene contenido de TV.      |



 

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





