---
description: Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de 2 pases.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90fd5435498a8a0c247d9363f02e2e767b46c5ab17ce36cc5a41feab54ed5277
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113295"
---
# <a name="mfpkey_ravg-property"></a>Propiedad MFPKEY \_ PFG

Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de 2 pases.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

En VBR restringida y sin restricciones, este valor es la velocidad de bits media a lo largo de la duración del contenido.

Debe establecer este valor para ambos modos de codificación VBR de dos pases. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que haya terminado de codificar la secuencia. El codificador interpreta una solicitud para este valor como una señal de que la sesión de codificación ha terminado; el ejemplo siguiente que se procesa se trata como el principio de una nueva sesión.

Esta propiedad también se puede leer al final de una sesión de codificación VBR de un paso.

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

 

 




