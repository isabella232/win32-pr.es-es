---
description: Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Propiedad CODECAPI_AVEncVideoEncodeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705424"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>\_Propiedad AVEncVideoEncodeQP de CODECAPI

Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valor de propiedad

Un conjunto de campos de 4 16 bits que se usan para especificar el marco QPs en la codificación de QP fija.

Los campos son:

-   Bits 0-15: QP predeterminado
-   Bits 16-31: QP usado para I fotogramas
-   Bits 32-47: QP usado para fotogramas P
-   Bits 48-63: QP usado para los fotogramas B

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

Para garantizar un uso coherente en los distintos codificadores, debe suponer que los codificadores solo examinarán el QP predeterminado y pueden ignorar los valores de QP para las imágenes I/P/B.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

