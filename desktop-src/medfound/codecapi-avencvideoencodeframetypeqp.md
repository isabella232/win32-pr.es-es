---
description: Especifica los tipos de marco (I, P o B) a los que se aplica el parámetro de cuantificación (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ebd4a25f3779ce1c721eb3cb1188b487be4d313ae5dbeb02dd41e494f4c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743883"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>Propiedad CODECAPI \_ AVEncVideoEncodeFrameTypeQP

Especifica los tipos de marco (I, P o B) a los que se aplica el parámetro de cuantificación (QP).

## <a name="data-type"></a>Tipo de datos

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Observaciones

Para los codificadores que admiten la configuración de un parámetro de cuantificación (QP) para diferentes tipos de fotogramas (I, P, B), expondrán esta API además de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md). Si un codificador solo admite un único QP para todos los tipos de fotogramas, solo admitirán CODECAPI \_ AVEncVideoEncodeQP.

Se trata de una propiedad de codificación dinámica que significa que se puede establecer un nuevo valor en cualquier momento durante la sesión de codificación.

**Codificadores H.264/AVC:**

El codificador debe [**admitir GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Se usa un conjunto de cuatro campos de 16 bits para especificar los QP de marco en la codificación de QP fija. Los campos son:

-   **Bits 0-15:** QP usado para fotogramas I, intervalo válido \[ 0, 51 \] .
-   **Bits 16-31:** QP usado para fotogramas P, intervalo válido \[ 0, 51 \] .
-   **Bits 32-47:** QP usado para fotogramas B, intervalo válido \[ 0, 51\]
-   **Bits 48-63: reservados**

Cuando se admite este CodecAPI, los codificadores deben admitir la configuración de QP en el tipo de fotograma I, P y B.

El valor predeterminado debe ser 0x0000001a001a001a. QP igual a 26 para I, P y B.

Cuando [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selecciona una capa temporal específica, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) de CODECAPI AVEncVideoEncodeFrameTypeQP establecerá QP para fotogramas I, P y B en esa \_ capa temporal. De forma predeterminada, establece QP para fotogramas I, P y B en la capa temporal de capa temporal base 0.

[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) y [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) se usarán para definir y limitar el intervalo de QP para los QP de todos los tipos de imagen, I, P y B.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

