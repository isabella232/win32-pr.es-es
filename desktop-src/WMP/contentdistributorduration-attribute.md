---
title: Atributo ContentDistributorDuration
description: El atributo ContentDistributorDuration es la duración de la reproducción del elemento, en segundos.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- ContentDistributorDuration Media Player de Windows
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700004"
---
# <a name="contentdistributorduration-attribute"></a>Atributo ContentDistributorDuration

El atributo **ContentDistributorDuration** es la duración de la reproducción del elemento, en segundos.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)

## <a name="remarks"></a>Observaciones

Si el atributo **Duration** normal no está establecido (NULL) o 0, se devolverá en su lugar el valor de este atributo.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Duration (atributo)**](duration-attribute.md)
</dt> </dl>

 

 





