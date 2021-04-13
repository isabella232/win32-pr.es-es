---
description: Valor que define el sistema de medida para un valor de profundidad en un fotograma de vídeo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564633"
---
# <a name="mf_mt_depth_measurement-attribute"></a>\_Atributo de \_ medición de profundidad MF MT \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Valor que define el sistema de medida para un valor de profundidad en un fotograma de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este valor es un miembro de la enumeración [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Si este atributo no está presente, se supone que es **DistanceToFocalPlane**. Normalmente, la distancia al plano focal es más fácil de consumir en un sistema de coordenadas euclidiana 3D.

![Ilustración de distancetofocalplane](images/distance-to-focal-plane.png)

El formato de distancia al centro focal es normalmente datos sin procesar del sensor, como la hora de las cámaras de vuelo.

![Ilustración de distancetoopticalcenter](images/distance-to-optical-center.png)

Las cámaras de profundidad no pueden detectar la profundidad de todos los píxeles. Cuando la confianza de un píxel es baja, debido a material, oclusión o fuera del intervalo, etc., el valor de profundidad en ese píxel puede ser no válido.

Cuando un valor de píxel de profundidad es 0, el píxel no es válido.

Algunas cámaras de profundidad adjuntan metadatos de máscara de archivos para cada píxel, además del valor de profundidad, para representar la razón por la que la profundidad del píxel no es válida, debido a material, oclusión o fuera del intervalo, etc. Se recomienda evitar la Asociación de metadatos como bits en valor de profundidad, ya que normalmente dará lugar a dificultades al usar estos valores en el sombreador de píxeles. En lugar. se recomienda usar un búfer de imagen 8 bits independiente con la misma resolución y adjuntarlo como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Estos metadatos varían para cada proveedor de la cámara y no están estandarizados por la plataforma. Se recomienda usar 16 bits completos para el valor de profundidad a fin de facilitar el procesamiento de bajada y el uso de un valor fijo como 0 para la invalidación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




