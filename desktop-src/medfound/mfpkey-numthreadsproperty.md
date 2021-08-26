---
description: Especifica el número de subprocesos que usará el codificador.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac8b6ec040ba07a2e38b1e9d8e2df6cf0fcbfcdbba14481e9b50379ecc10df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953915"
---
# <a name="mfpkey_numthreads-property"></a>Propiedad NUMTHREADS de MFPKEY \_

Especifica el número de subprocesos que usará el codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="remarks"></a>Comentarios

Este valor está pensado para dividir la codificación en varios subprocesos para aprovechar las ventajas de los equipos con varios procesadores. Dividir las tareas de codificación en varios subprocesos puede provocar una ligera disminución de la calidad en comparación con un único subproceso.

Para el codificador de vídeo (wmvencod.dll) publicado con Windows XP y Windows Vista, esta propiedad debe establecerse en 1, 2 o 4. Otros valores se redondearán hacia abajo.

Para el codificador de vídeo (wmvencod.dll) publicado con Windows 7, esta propiedad debe establecerse en 1, 2, 4 u 8. Otros valores se redondearán hacia abajo.

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

 

 




