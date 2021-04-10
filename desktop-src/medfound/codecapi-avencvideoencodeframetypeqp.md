---
description: Especifica los tipos de fotogramas (I, P o B) a los que se aplica el parámetro de cuantificación (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Propiedad CODECAPI_AVEncVideoEncodeFrameTypeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153675"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>\_Propiedad AVEncVideoEncodeFrameTypeQP de CODECAPI

Especifica los tipos de fotogramas (I, P o B) a los que se aplica el parámetro de cuantificación (QP).

## <a name="data-type"></a>Tipo de datos

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Observaciones

En el caso de los codificadores que admiten la configuración de un parámetro de cuantificación (QP) para diferentes tipos de fotogramas (I, P, B), expondrán esta API además de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md). Si un codificador solo admite un único QP para todos los tipos de fotogramas, solo admitirá CODECAPI \_ AVEncVideoEncodeQP.

Se trata de una propiedad de codificación dinámica que significa que se puede establecer un nuevo valor en cualquier momento durante la sesión de codificación.

**Codificadores H. 264/AVC:**

El codificador debe admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Se utiliza un conjunto de campos de 4 16 bits para especificar el marco QPs en la codificación de QP fija. Los campos son:

-   **Bits 0-15:** QP usado para I-frames, intervalo válido de \[ 0 a 51 \] .
-   **Bits 16-31:** QP usado para los fotogramas P, intervalo válido de \[ 0 a 51 \] .
-   **Bits 32-47:** QP usado para los fotogramas B, intervalo válido de \[ 0 a 51\]
-   **Bits 48-63:** reservado

Cuando se admite este CodecAPI, los codificadores deben admitir la configuración de QP en el tipo de fotograma I, P y B.

El valor predeterminado debe ser 0x0000001a001a001a. QP igual a 26 para I, P y B.

Cuando [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selecciona una capa temporal específica, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) de CODECAPI \_ AVEncVideoEncodeFrameTypeQP establecerá QP para los fotogramas I, P y B en esa capa temporal. De forma predeterminada, establece QP para los fotogramas I, P y B en el nivel temporal de la capa temporal base 0.

[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) y [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) se usarán para definir y limitar el intervalo de QP para QPs de todos los tipos de imagen, I, P y B.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

