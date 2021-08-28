---
description: Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propiedad AVEncVideoOutputFrameRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f1e1105ad98564b8d837f35e574be25bcd6cb9506a2adddbc115129fcb65564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540675"
---
# <a name="avencvideooutputframerate-property"></a>Propiedad AVEncVideoOutputFrameRate

Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoOutputFrameRate**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es una relación que define la velocidad de fotogramas. Los 32 bits superiores contienen el numerador y los 32 bits inferiores contienen el denominador. En la tabla siguiente se muestran las velocidades de fotogramas comunes, en fotogramas por segundo.



| Velocidad de fotogramas | Proporción      |
|------------|------------|
| 23.97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29.97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59.94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>Comentarios

Las aplicaciones pueden establecer esta propiedad para especificar la velocidad de fotogramas de salida. Los codificadores también pueden devolver esta propiedad como una funcionalidad. Dependiendo del codificador, el valor puede estar restringido a la velocidad de fotogramas de entrada. Si no es así, el codificador puede convertir internamente la velocidad de fotogramas. Vea [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

