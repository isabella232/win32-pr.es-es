---
description: Valor que define el sistema de medida para un valor de profundidad en un fotograma de vídeo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a292e5a96cec7490917ef0bb897a9a7a67dd303d29692bf6db5ff58e1d4388c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605809"
---
# <a name="mf_mt_depth_measurement-attribute"></a>Atributo MF \_ MT \_ DEPTH \_ MEASUREMENT

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Valor que define el sistema de medida para un valor de profundidad en un fotograma de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este valor es miembro de la [**\_ enumeración MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Si este atributo no está presente, se supone **que es DistanceToFocalPlane**. La distancia al plano focal suele ser más fácil de consumir en un sistema de coordenadas euclidiano 3D.

![ilustración de distancetofocalplane](images/distance-to-focal-plane.png)

La distancia al formato del centro focal suele ser datos sin procesar del sensor, como la hora de las cámaras de vuelo.

![ilustración de distancetoopticalcenter](images/distance-to-optical-center.png)

Las cámaras de profundidad no pueden entender la profundidad de todos los píxeles. Cuando la confianza de un píxel es baja, debido a material, oclusión o fuera del intervalo, etc., el valor de profundidad de ese píxel puede no ser válido.

Cuando un valor de píxel de profundidad es 0, el píxel no es válido.

Algunas cámaras de profundidad adjuntan metadatos de máscara de bits para cada píxel además del valor de profundidad para representar el motivo por el que la profundidad del píxel no es válida, debido a material, oclusión o fuera del intervalo, etc. Se recomienda evitar adjuntar estos metadatos como bits en el valor de profundidad, ya que normalmente dará lugar a dificultades al usar estos valores en el sombreador de píxeles. en lugar de. Se recomienda usar un búfer de imagen de 8 bits independiente con la misma resolución y adjuntarlo como atributo de [**LAMUEJEMPLO.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Estos metadatos varían para cada proveedor de cámara y no están estandarizados por la plataforma. Se recomienda usar 16 bits completos para el valor de profundidad para facilitar el procesamiento de bajada y el uso de un valor fijo como 0 para la invalidación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




