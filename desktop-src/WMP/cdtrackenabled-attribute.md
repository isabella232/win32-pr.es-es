---
title: Atributo CDTrackEnabled
description: El atributo CDTrackEnabled indica si la pista está habilitada para la reproducción.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- CDTrackEnabled Media Player de Windows
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700308"
---
# <a name="cdtrackenabled-attribute"></a>Atributo CDTrackEnabled

El atributo **CDTrackEnabled** indica si la pista está habilitada para la reproducción.

## <a name="applies-to"></a>Se aplica a

-   [Pistas de CD](cd-track-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en la memoria caché de la biblioteca.

Al reproducir un CD en Windows Media Player, el usuario puede seleccionar una pista y especificar que no se debe reproducir. Este valor de este atributo es true si se puede reproducir la pista o false si el usuario especificó que no se debe reproducir la pista.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





