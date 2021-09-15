---
description: Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en calidad.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: MFPKEY_WMAENC_AVGBYTESPERSEC propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef88b9ea0cf46829a33cb7b9901c7c9f844c1e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475675"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>Propiedad \_ \_ AVGBYTESPERSEC de MFPKEY WMAENC

Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en calidad.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede obtener este valor desde el descodificador después de codificar la secuencia.

El descodificador de audio requiere este valor para descomprimir correctamente el contenido.

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

 

 




