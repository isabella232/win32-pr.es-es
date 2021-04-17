---
description: Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de dos pasos, de velocidad de bits variable (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Propiedad MFPKEY_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706209"
---
# <a name="mfpkey_ravg-property"></a>\_Propiedad RAVG de MFPKEY

Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de dos pasos, de velocidad de bits variable (VBR).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

En VBR restringida y sin restricciones, este valor es la velocidad de bits promedio a lo largo de la duración del contenido.

Debe establecer este valor para ambos modos de codificación VBR de dos pasos. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que termine de codificar la secuencia. El codificador interpreta una solicitud para este valor como una señal en la que se ha superado la sesión de codificación; el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.

Esta propiedad también se puede leer al final de una sesión de codificación VBR de 1 paso.

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

 

 




