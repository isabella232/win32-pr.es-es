---
description: Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720490"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>\_Atributo ROIRectangle de MFSampleExtension

Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.

## <a name="data-type"></a>Tipo de datos

**[**ROI \_ ÁREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** almacenada como **BLOB**

## <a name="remarks"></a>Observaciones

Después de configurar correctamente [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) en un valor distinto de cero en un MFT del codificador, la aplicación puede establecer este atributo en los ejemplos de entrada y esperar que se respete.

Si [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) no se establece en un valor distinto de cero, el \_ atributo MFSampleExtension ROIRectangle se omite en los ejemplos de entrada.

MFSampleExtension \_ ROIRectangle se establece en una muestra de entrada y solo se aplica al ejemplo de entrada actual.

El campo **QPDelta** de la estructura de [**\_ área de ROI**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) especifica el delta del parámetro de cuantificación para la región especificada desde el resto del marco. Si **QPDelta** es positivo, indica que la aplicación desea que el rectángulo tenga una calidad inferior que el resto del marco.

**Codificadores H. 264/AVC:** **QPDelta** debe estar entre \[ -25, + 25 \] . El codificador garantizará que la QP final esté en un intervalo válido para el estándar de vídeo.

No es necesario que la región especificada sea de MB alineada. Los codificadores tienen flexibilidad para decidir el límite real. Se recomienda cubrir toda la región especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




