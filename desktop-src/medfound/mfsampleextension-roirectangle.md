---
description: Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311b17cab20de16a83d145563e8ba0b8ead6f055428ffc6a3823c99deab05fc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240330"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>Atributo MFSampleExtension \_ ROIRectangle

Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.

## <a name="data-type"></a>Tipo de datos

**[**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** almacenado como **BLOB**

## <a name="remarks"></a>Comentarios

Después de establecer [correctamente CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) en un valor distinto de cero en un MFT del codificador, la aplicación puede establecer este atributo en los ejemplos de entrada y esperar que se respeta.

Si [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) no está establecido en un valor distinto de cero, el atributo MFSampleExtension ROIRectangle se omite en los ejemplos \_ de entrada.

MFSampleExtension \_ ROIRectangle se establece en un ejemplo de entrada y solo se aplica al ejemplo de entrada actual.

El **campo QPDelta** de la estructura [**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) especifica el delta del parámetro de cuantificación para la región especificada del resto del marco. Si **QPDelta** es positivo, esto indica que la aplicación quiere que el rectángulo tenga una calidad inferior que el resto del marco.

**Codificadores H.264/AVC:** **QPDelta** debe estar entre \[ -25 y +25 \] . El codificador debe asegurarse de que el QP final está en un intervalo válido para el estándar de vídeo.

No es necesario que la región especificada esté alineada con MB. Los codificadores tienen flexibilidad para decidir el límite real. Se recomienda cubrir toda la región especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




