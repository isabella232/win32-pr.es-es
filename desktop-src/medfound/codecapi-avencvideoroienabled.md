---
description: Indica si \_ el atributo MFSampleExtension ROIRectangle establecido en el ejemplo de entrada se respetará o no.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: Propiedad CODECAPI_AVEncVideoROIEnabled (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360110"
---
# <a name="codecapi_avencvideoroienabled-property"></a>\_Propiedad AVEncVideoROIEnabled de CODECAPI

Indica si el atributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) establecido en el ejemplo de entrada se respetará o no.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Observaciones

El valor predeterminado es 0.

Si un MFT del codificador acepta un valor distinto de cero, se espera que el codificador respete el atributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) establecido en la muestra de entrada.

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

 

 




