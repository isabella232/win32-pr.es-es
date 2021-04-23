---
description: Esta propiedad se usa para indicar qué versión del conjunto de propiedades De cambio de frecuencia debe usar el descodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910223"
---
# <a name="am_rate_userateversion-property"></a>Propiedad \_ \_ UseRateVersion de AM RATE

Esta propiedad se usa para indicar qué versión del conjunto de propiedades De cambio de frecuencia debe usar el descodificador. El valor es un **tipo WORD.** El byte de orden superior contiene el número de versión secundaria y el byte de orden bajo contiene el byte de orden bajo. Por lo tanto, la versión 1.1 se señala con el valor 0x0101.

Si el descodificador no admite la versión especificada, debe producir un error en la llamada a [**IKsPropertySet::Set**](ikspropertyset-set.md) y devolver E \_ NOINTERFACE. Si el filtro de origen no establece la versión, el descodificador debe tener como valor predeterminado la versión 1.0.



| Etiqueta | Value |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange |
| Id. de propiedad       | AM \_ RATE \_ UseRateVersion      |
| Tipo de datos         | **WORD**                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)
</dt> </dl>

 

 




