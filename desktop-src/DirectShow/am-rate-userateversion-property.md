---
description: Esta propiedad se usa para indicar qué versión del conjunto de propiedades de cambio de velocidad debe usar el descodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Propiedad AM_RATE_UseRateVersion (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660948"
---
# <a name="am_rate_userateversion-property"></a>\_Propiedad UseRateVersion de tasa AM \_

Esta propiedad se usa para indicar qué versión del conjunto de propiedades de cambio de velocidad debe usar el descodificador. El valor es un tipo de **palabra** . El byte de orden superior contiene el número de versión secundaria y el byte de orden inferior contiene el byte de orden inferior. Por lo tanto, la versión 1,1 se señala con el valor 0x0101.

Si el descodificador no admite la versión especificada, se debería producir un error en la llamada a [**IKsPropertySet:: set**](ikspropertyset-set.md) y devolver E \_ nointerface. Si el filtro de origen no establece la versión, el descodificador debería tener como valor predeterminado la versión 1,0.



|                   |                               |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | \_TSRateChange KSPROPSETID \_ AM |
| Id. de propiedad       | Tasa de AM \_ \_ UseRateVersion      |
| Tipo de datos         | **WORD**                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




