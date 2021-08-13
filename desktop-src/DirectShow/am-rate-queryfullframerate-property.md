---
description: Esta propiedad consulta al descodificador la velocidad máxima de fotogramas completos que admite el descodificador. El tipo de datos de esta propiedad es una estructura \_ QueryRate de AM.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate (Propiedad, Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ceb938ac3fd0ea5f7f58b340f4b57fd6a722650cd3225702cbb74b1644045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664114"
---
# <a name="am_rate_queryfullframerate-property"></a>Propiedad \_ \_ QueryFullFrameRate de AM RATE

Esta propiedad consulta al descodificador la velocidad máxima de fotogramas completos que admite el descodificador. El tipo de datos de esta propiedad es una **estructura \_ QueryRate de AM.**

Esta propiedad se define para la versión 1.1 de este conjunto de propiedades; vea [**Am \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Etiqueta | Value |
|-------------------|---------------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange         |
| Id. de propiedad       | Propiedad \_ \_ QueryFullFrameRate de AM RATE |
| Tipo de datos         | [**Velocidad \_ de consulta de AM**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Observaciones

Si la velocidad de reproducción supera la velocidad máxima del descodificador, el filtro de origen envía grupos de muestras continuas separadas por discontinuidades. Las marcas de tiempo saltan entre las discontinuidades. El filtro de origen podría hacer esto incluso si la velocidad de reproducción está dentro de la velocidad máxima del descodificador, ya que puede haber otros factores, como la E/S de disco, que limiten la velocidad de reproducción completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)
</dt> </dl>

 

 




