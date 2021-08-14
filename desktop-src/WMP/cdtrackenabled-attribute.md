---
title: Atributo CDTrackEnabled
description: El atributo CDTrackEnabled indica si la pista está habilitada para la reproducción.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- CdTrackEnabled Attribute Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a86c94c2c1b44327cdbfb35544c3e0b5b34d25885215d78dbec0ec084d056e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342688"
---
# <a name="cdtrackenabled-attribute"></a>Atributo CDTrackEnabled

El **atributo CDTrackEnabled** indica si la pista está habilitada para la reproducción.

## <a name="applies-to"></a>Se aplica a

-   [Pistas de CD](cd-track-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo solo se almacena en la memoria caché de la biblioteca.

Al reproducir un CD en Reproductor de Windows Media, el usuario puede seleccionar una pista y especificar que no se debe reproducir. Este valor de este atributo es True si se puede reproducir la pista o False si el usuario especificó que no se debe reproducir la pista.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





