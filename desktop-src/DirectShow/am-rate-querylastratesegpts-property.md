---
description: Esta propiedad consulta al descodificador la hora de inicio del cambio de velocidad que se ha puesto en cola más recientemente, independientemente de su posición en la cola de cambio de frecuencia.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910273"
---
# <a name="am_rate_querylastratesegpts-property"></a>Consulta \_ AM \_ RATELastRateSegPTS Propiedad

Esta propiedad consulta al descodificador la hora de inicio del cambio de velocidad que se ha puesto en cola más recientemente, independientemente de su posición en la cola de cambio de frecuencia.

Esta propiedad se define para la versión 1.1 de este conjunto de propiedades; vea [**Am \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Etiqueta | Value |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange |
| Id. de propiedad       | Consulta \_ AM \_ RATELastRateSegPTS |
| Tipo de datos         | **HORA DE \_ REFERENCIA**           |



 

## <a name="remarks"></a>Comentarios

El filtro de origen puede usar esta propiedad para sincronizar los cambios de velocidad en varias secuencias de audio y vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)
</dt> </dl>

 

 




