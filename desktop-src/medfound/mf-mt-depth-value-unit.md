---
description: Valor que define las unidades de un valor de profundidad en un fotograma de vídeo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca57fa5cf72be266ac58ee504b1d4b7c4f2506646f33295e468d2ed0781ab8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060645"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>Atributo MF \_ MT \_ DEPTH VALUE \_ \_ UNIT

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Valor que define las unidades de un valor de profundidad en un fotograma de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

El valor de unidad es un valor UINT64 en nanometers, en el intervalo de 1e a 9 metros. Si este valor no está presente, el valor predeterminado de la unidad es 1e-3, lo que indica que cada nivel de píxel se mide en 1 milímetro en el espacio físico.

Las cámaras de profundidad no pueden entender la profundidad de todos los píxeles. Cuando la confianza de un píxel es baja, debido a material, oclusión o fuera del intervalo, etc., el valor de profundidad de ese píxel puede no ser válido.

Cuando un valor de píxel de profundidad es 0, el píxel no es válido.

Algunas cámaras de profundidad adjuntan metadatos de máscara de bits para cada píxel además del valor de profundidad para representar el motivo por el que la profundidad del píxel no es válida, debido a material, oclusión o fuera del intervalo, etc. Se recomienda evitar adjuntar estos metadatos como bits en el valor de profundidad, ya que normalmente dará lugar a dificultades al usar estos valores en el sombreador de píxeles. en lugar de. Se recomienda usar un búfer de imagen de 8 bits independiente con la misma resolución y adjuntarlo como atributo de [**LAMUEJEMPLO.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Estos metadatos varían para cada proveedor de cámara y no están estandarizados por la plataforma. Se recomienda usar 16 bits completos para el valor de profundidad para facilitar el procesamiento de bajada y el uso de un valor fijo como 0 para la invalidación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




