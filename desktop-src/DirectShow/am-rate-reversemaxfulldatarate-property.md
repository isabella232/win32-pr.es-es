---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910243"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>Propiedad AM \_ RATE \_ ReverseMaxFullDataRate

Se aplica a Windows Vista y versiones posteriores.

Devuelve la velocidad máxima de reproducción inversa del descodificador. El valor de la propiedad es el valor absoluto de la velocidad inversa máxima x 10000. Por ejemplo, si la velocidad inversa máxima es -2,0, el valor de esta propiedad es 20000.

El tipo de datos de esta propiedad **es AM \_ MaxFullDataRate,** que es para `typedef` **LONG.**

Esta propiedad es de solo lectura.



| Etiqueta | Value |
|-------------------|----------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange    |
| Id. de propiedad       | AM \_ RATE \_ ReverseMaxFullDataRate |
| Tipo de datos         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Comentarios

Los descodificadores que admiten la reproducción inversa sin problemas deben exponer esta propiedad. Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista (Mejoras](dvd-playback-enhancements-in-windows-vista.md)de reproducción de DVD en Windows Vista).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)
</dt> </dl>

 

 




