---
description: Especifica el número de subprocesos que usará el codificador.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268852"
---
# <a name="mfpkey_numthreads-property"></a>Propiedad NUMTHREADS de MFPKEY \_

Especifica el número de subprocesos que usará el codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="remarks"></a>Observaciones

Este valor está pensado para dividir la codificación en varios subprocesos para aprovechar las ventajas de los equipos con varios procesadores. Dividir las tareas de codificación en varios subprocesos puede provocar una ligera disminución de la calidad en comparación con un único subproceso.

Para el codificador de vídeo (wmvencod.dll) publicado con Windows XP y Windows Vista, esta propiedad debe establecerse en 1, 2 o 4. Otros valores se redondean hacia abajo.

Para el codificador de vídeo (wmvencod.dll) publicado con Windows 7, esta propiedad debe establecerse en 1, 2, 4 u 8. Otros valores se redondean hacia abajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




