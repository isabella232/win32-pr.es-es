---
description: Establece la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se alimentan al codificador.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Propiedad CODECAPI_AVEncMaxFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652355"
---
# <a name="codecapi_avencmaxframerate-property"></a>\_Propiedad AVEncMaxFrameRate de CODECAPI

Establece la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se alimentan al codificador.

## <a name="data-type"></a>Tipo de datos

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Observaciones

Esta propiedad permite al llamador especificar la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se alimentan al codificador. Esto proporciona al codificador una indicación de la frecuencia con la que será necesario procesar los fotogramas entrantes. Esto resulta útil para los codificadores que se establecen en una configuración de estado de energía determinada en función de la resolución y la velocidad de fotogramas del vídeo de origen.

La velocidad de fotogramas se expresa como una proporción. Los 32 superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1. Si la velocidad de fotogramas es 29,97 fps, la relación es 30000/1001.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

