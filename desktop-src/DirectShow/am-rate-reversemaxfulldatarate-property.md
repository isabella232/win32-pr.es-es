---
description: 'AM_RATE_ReverseMaxFullDataRate propiedad: se aplica a Windows Vista y versiones posteriores.'
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate (Propiedad, Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c02007ec0b8f7b3f14dee8490f69d654a99ad11480512408efdc656bbbc8561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002380"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>Propiedad AM \_ RATE \_ ReverseMaxFullDataRate

Se aplica a Windows Vista y versiones posteriores.

Devuelve la velocidad máxima de reproducción inversa del descodificador. El valor de la propiedad es el valor absoluto de la velocidad inversa máxima x 10000. Por ejemplo, si la velocidad inversa máxima es -2,0, el valor de esta propiedad es 20000.

El tipo de datos de esta propiedad **es AM \_ MaxFullDataRate,** que es para `typedef` **LONG.**

Esta propiedad es de solo lectura.



| Etiqueta | Valor |
|-------------------|----------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange    |
| Id. de propiedad       | AM \_ RATE \_ ReverseMaxFullDataRate |
| Tipo de datos         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Comentarios

Los descodificadores que admiten la reproducción inversa sin problemas deben exponer esta propiedad. Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md)(Mejoras de reproducción de DVD Windows Vista).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)
</dt> </dl>

 

 




