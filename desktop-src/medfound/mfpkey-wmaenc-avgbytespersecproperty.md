---
description: Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en calidad.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: MFPKEY_WMAENC_AVGBYTESPERSEC propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfadc41e9f2c9f4410bc84c6d8bf23f30c559b96c83abba80beb719e8ccb8eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953305"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>Propiedad MFPKEY \_ WMAENC \_ AVGBYTESPERSEC

Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en calidad.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Puede obtener este valor del descodificador después de codificar la secuencia.

El descodificador de audio requiere este valor para descomprimir correctamente el contenido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




