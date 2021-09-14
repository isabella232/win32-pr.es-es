---
description: 'AM_RATE_ReverseMaxFullDataRate propiedad: se aplica a Windows Vista y versiones posteriores.'
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162337"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>Propiedad \_ \_ REVERSEMAXFullDataRate de AM RATE

Se aplica a Windows Vista y versiones posteriores.

Devuelve la velocidad máxima de reproducción inversa del descodificador. El valor de la propiedad es el valor absoluto de la velocidad inversa máxima x 10000. Por ejemplo, si la velocidad inversa máxima es -2,0, el valor de esta propiedad es 20000.

El tipo de datos de esta propiedad **es AM \_ MaxFullDataRate**, que es para `typedef` **LONG.**

Esta propiedad es de solo lectura.



| Etiqueta | Value |
|-------------------|----------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange    |
| Id. de propiedad       | AM \_ RATE \_ ReverseMaxFullDataRate |
| Tipo de datos         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Observaciones

Los descodificadores que admiten la reproducción inversa sin problemas deben exponer esta propiedad. Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




