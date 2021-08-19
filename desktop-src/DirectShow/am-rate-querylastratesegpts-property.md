---
description: Esta propiedad consulta al descodificador la hora de inicio del cambio de velocidad que se ha puesto en cola más recientemente, independientemente de su posición en la cola de cambio de frecuencia.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e7b54e618829d9768b4d08a0a76defcf2c91758be6b916b6e570b368191e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824839"
---
# <a name="am_rate_querylastratesegpts-property"></a>Consulta \_ AM \_ RATELastRateSegPTS Propiedad

Esta propiedad consulta al descodificador la hora de inicio del cambio de velocidad que se ha puesto en cola más recientemente, independientemente de su posición en la cola de cambio de frecuencia.

Esta propiedad se define para la versión 1.1 de este conjunto de propiedades; vea [**Am \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Etiqueta | Valor |
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)
</dt> </dl>

 

 




