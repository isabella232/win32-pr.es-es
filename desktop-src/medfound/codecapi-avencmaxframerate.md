---
description: Establece la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se introducen en el codificador.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb4202dd2079cc013560947ef11581cdb24b92ad0aaaf544e12923d5e46b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974934"
---
# <a name="codecapi_avencmaxframerate-property"></a>Propiedad CODECAPI \_ AVEncMaxFrameRate

Establece la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se introducen en el codificador.

## <a name="data-type"></a>Tipo de datos

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Comentarios

Esta propiedad permite al autor de la llamada especificar la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se introducen en el codificador. Esto proporciona al codificador una indicación de la velocidad que necesitará para procesar los fotogramas entrantes. Esto es útil para los codificadores que se establecen en una configuración de estado de energía determinada en función de la resolución y la velocidad de fotogramas del vídeo de origen.

La velocidad de fotogramas se expresa como una relación. Los 32 bits superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (fps), la proporción es de 30/1. Si la velocidad de fotogramas es de 29,97 fps, la relación es de 30 000/1001.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

