---
description: Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propiedad AVEncVideoOutputFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805822"
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
| 23,97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29,97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59,94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para especificar la velocidad de fotogramas de salida. Los codificadores también pueden devolver esta propiedad como una capacidad. Dependiendo del codificador, el valor puede estar restringido a la velocidad de fotogramas de entrada. En caso contrario, el codificador puede convertir la velocidad de fotogramas internamente. Vea la [**propiedad AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

