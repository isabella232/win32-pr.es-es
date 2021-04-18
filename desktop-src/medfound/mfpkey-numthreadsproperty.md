---
description: Especifica el número de subprocesos que utilizará el codificador.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Propiedad MFPKEY_NUMTHREADS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544910"
---
# <a name="mfpkey_numthreads-property"></a>\_Propiedad NUMTHREADS de MFPKEY

Especifica el número de subprocesos que utilizará el codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="remarks"></a>Observaciones

Este valor está pensado para dividir la codificación en varios subprocesos con el fin de aprovechar los equipos con varios procesadores. Dividir las tareas de codificación en varios subprocesos puede provocar una ligera disminución de la calidad en comparación con un solo subproceso.

Para el codificador de vídeo (wmvencod.dll) lanzado con Windows XP y Windows Vista, esta propiedad debe establecerse en 1, 2 o 4. Otros valores se redondean hacia abajo.

En el caso del codificador de vídeo (wmvencod.dll) lanzado con Windows 7, esta propiedad debe establecerse en 1, 2, 4 u 8. Otros valores se redondean hacia abajo.

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

 

 




