---
description: Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción restringida de velocidad de bits variable de dos pases (VBR).
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e80f679d0ed1213a54a4f22bc5d8bfc79f41b93fa05c446c8b6ed0f589183b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398405"
---
# <a name="mfpkey_rmax-property"></a>Propiedad MFPKEY \_ RMAX

Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción restringida de velocidad de bits variable de dos pases (VBR).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay valor predeterminado.

## <a name="remarks"></a>Comentarios

Este valor representa la velocidad de bits máxima para la reproducción. El valor de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) se usa para describir el búfer en términos de esta velocidad de bits; en efecto, la VBR restringida es similar a la velocidad de bits constante (CBR) que usa este valor como velocidad de bits. Sin embargo, una secuencia DE VBR restringida se puede reproducir a una velocidad de bits inferior, siempre y cuando se incremente el búfer.

Debe establecer este valor para la codificación VBR de dos pases con restricciones máximas. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que haya terminado de codificar la secuencia. El codificador interpreta una solicitud para este valor como una señal de que la sesión de codificación ha terminado; el ejemplo siguiente que se procesa se trata como el principio de una nueva sesión.

Normalmente, este valor es de dos a tres veces mayor que el valor de [MFPKEY \_ PFKEY DEG.](mfpkey-ravgproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




