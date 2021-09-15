---
description: Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción restringida de velocidad de bits variable de dos pases (VBR).
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468621"
---
# <a name="mfpkey_rmax-property"></a>Propiedad MFPKEY \_ RMAX

Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción restringida de velocidad de bits variable de dos pases (VBR).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay valor predeterminado.

## <a name="remarks"></a>Observaciones

Este valor representa la velocidad de bits máxima para la reproducción. El valor de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) se usa para describir el búfer en términos de esta velocidad de bits; en efecto, la VBR restringida es similar a la velocidad de bits constante (CBR) que usa este valor como velocidad de bits. Sin embargo, una secuencia DE VBR restringida se puede reproducir a una velocidad de bits inferior, siempre y cuando se incremente el búfer.

Debe establecer este valor para la codificación VBR de dos pases con restricciones máximas. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que haya terminado de codificar la secuencia. El codificador interpreta una solicitud para este valor como una señal de que la sesión de codificación ha terminado; el ejemplo siguiente que se procesa se trata como el principio de una nueva sesión.

Normalmente, este valor es de dos a tres veces mayor que el valor de [MFPKEY \_ PFKEY DEG.](mfpkey-ravgproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




