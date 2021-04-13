---
description: Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en la calidad.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: Propiedad MFPKEY_WMAENC_AVGBYTESPERSEC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef88b9ea0cf46829a33cb7b9901c7c9f844c1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543966"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>\_ \_ Propiedad AVGBYTESPERSEC de MFPKEY WMAENC

Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en la calidad.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede obtener este valor desde el descodificador después de codificar la secuencia.

Este valor es necesario para que el descodificador de audio descomprima correctamente el contenido.

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

 

 




