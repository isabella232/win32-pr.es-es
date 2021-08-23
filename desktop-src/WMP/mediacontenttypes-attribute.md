---
title: Atributo MediaContentTypes
description: El atributo MediaContentTypes especifica el tipo de contenido del elemento.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Atributo MediaContentTypes Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca3c422083954554db76657a0bb9cc10062fd878a9ebf4b31f4dc88734ac1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996245"
---
# <a name="mediacontenttypes-attribute"></a>Atributo MediaContentTypes

El **atributo MediaContentTypes** especifica el tipo de contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Listas](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentarios

Este atributo puede ser uno de los siguientes valores:



| Value | Significado                                |
|-------|----------------------------------------|
| 1     | La lista de reproducción contiene contenido de audio.   |
| 2     | Que se va a proporcionar.                        |
| 3     | La lista de reproducción contiene contenido de audio.   |
| 4     | La lista de reproducción contiene contenido de vídeo.   |
| 5     | La lista de reproducción contiene contenido de imagen. |
| 6     | La lista de reproducción contiene contenido de televisión.      |



 

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





