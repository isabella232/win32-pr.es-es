---
description: Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580281"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>Atributo MFSampleExtension \_ ROIRectangle

Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.

## <a name="data-type"></a>Tipo de datos

**[**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** almacenado como **BLOB**

## <a name="remarks"></a>Observaciones

Después de establecer [correctamente CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) en un valor distinto de cero en un MFT del codificador, la aplicación puede establecer este atributo en los ejemplos de entrada y esperar que se respeta.

Si [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) no está establecido en un valor distinto de cero, el atributo MFSampleExtension ROIRectangle se omite en los ejemplos \_ de entrada.

MFSampleExtension \_ ROIRectangle se establece en un ejemplo de entrada y solo se aplica al ejemplo de entrada actual.

El **campo QPDelta** de la estructura [**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) especifica el delta del parámetro de cuantificación para la región especificada del resto del marco. Si **QPDelta** es positivo, esto indica que la aplicación quiere que el rectángulo tenga una calidad inferior que el resto del marco.

**Codificadores H.264/AVC:** **QPDelta** debe estar entre \[ -25 y +25 \] . El codificador debe asegurarse de que el QP final está en un intervalo válido para el estándar de vídeo.

No es necesario que la región especificada esté alineada con MB. Los codificadores tienen flexibilidad para decidir el límite real. Se recomienda cubrir toda la región especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




