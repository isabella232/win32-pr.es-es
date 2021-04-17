---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Propiedad AM_RATE_ReverseMaxFullDataRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660951"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>\_Propiedad ReverseMaxFullDataRate de tasa AM \_

Se aplica a Windows Vista y versiones posteriores.

Devuelve la velocidad máxima de reproducción inversa del descodificador. El valor de la propiedad es el valor absoluto de la velocidad máxima inversa x 10000. Por ejemplo, si la velocidad máxima inversa es-2,0, el valor de esta propiedad es 20000.

El tipo de datos de esta propiedad es **AM \_ MaxFullDataRate**, que es un `typedef` para **Long**.

Esta propiedad es de solo lectura.



|                   |                                  |
|-------------------|----------------------------------|
| GUID del conjunto de propiedades | \_TSRateChange KSPROPSETID \_ AM    |
| Id. de propiedad       | Tasa de AM \_ \_ ReverseMaxFullDataRate |
| Tipo de datos         | **\_MAXFULLDATARATE AM**          |



 

## <a name="remarks"></a>Observaciones

Los descodificadores que admiten la reproducción fluida inversa deben exponer esta propiedad. Para obtener más información, consulte [mejoras en la reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




