---
description: Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción de velocidad de bits variable (VBR) limitada de dos pasos.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Propiedad MFPKEY_RMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276289"
---
# <a name="mfpkey_rmax-property"></a>\_Propiedad RMAX de MFPKEY

Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción de velocidad de bits variable (VBR) limitada de dos pasos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay valor predeterminado.

## <a name="remarks"></a>Observaciones

Este valor representa la velocidad de bits máxima para la reproducción. El valor de [MFPKEY \_ Bmax](mfpkey-bmaxproperty.md) se usa para describir el búfer en términos de esta velocidad de bits; de hecho, la VBR restringida es similar a la velocidad de bits constante (CBR) con este valor como la velocidad de bits. Sin embargo, una secuencia VBR restringida se puede reproducir a una velocidad de bits más baja, siempre y cuando aumente el búfer.

Debe establecer este valor para la codificación VBR de dos pases restringida. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que termine de codificar la secuencia. El codificador interpreta una solicitud para este valor como una señal en la que se ha superado la sesión de codificación; el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.

Normalmente, este valor es de dos a tres veces mayor que el valor de [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




