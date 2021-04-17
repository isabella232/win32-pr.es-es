---
description: Esta propiedad consulta el descodificador para la velocidad máxima de fotogramas completa que admite el descodificador. El tipo de datos de esta propiedad es una \_ estructura AM QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Propiedad AM_RATE_QueryFullFrameRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690631"
---
# <a name="am_rate_queryfullframerate-property"></a>\_Propiedad QueryFullFrameRate de tasa AM \_

Esta propiedad consulta el descodificador para la velocidad máxima de fotogramas completa que admite el descodificador. El tipo de datos de esta propiedad es una estructura **AM \_ QueryRate** .

Esta propiedad se define para la versión 1,1 de este conjunto de propiedades; vea [**\_ tasa AM \_ UseRateVersion**](am-rate-userateversion-property.md).



|                   |                                       |
|-------------------|---------------------------------------|
| GUID del conjunto de propiedades | \_TSRateChange KSPROPSETID \_ AM         |
| Id. de propiedad       | \_Propiedad QueryFullFrameRate de tasa AM \_ |
| Tipo de datos         | [**\_QUERYRATE AM**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Observaciones

Si la velocidad de reproducción supera la tasa máxima del descodificador, el filtro de origen envía grupos de muestras continuas separadas por discontinuidades. Las marcas de tiempo saltan entre las discontinuidades. El filtro de origen puede hacer esto incluso si la velocidad de reproducción está dentro de la velocidad máxima del descodificador, porque puede haber otros factores, como la e/s de disco, que limitan la velocidad de reproducción completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




