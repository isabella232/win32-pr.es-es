---
title: Atributo SyncOnly
description: El atributo SyncOnly es una representación de cadena de un valor booleano que Windows Media Player usa para determinar si una lista de reproducción solo está disponible para la sincronización.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- SyncOnly Media Player de Windows
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718681"
---
# <a name="synconly-attribute"></a>Atributo SyncOnly

El atributo **SyncOnly** es una representación de cadena de un valor **booleano** que Windows Media Player usa para determinar si una lista de reproducción solo está disponible para la sincronización.

## <a name="applies-to"></a>Se aplica a

-   [Reproducción](playlist-attributes-ref.md)

## <a name="remarks"></a>Observaciones

Un valor de 1 indica que la lista de reproducción solo está disponible para la sincronización y no puede aparecer en el nodo de **lista de reproducción automática** . Un valor de cero indica que la lista de reproducción puede aparecer en el nodo de **lista de reproducción automática** .

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





