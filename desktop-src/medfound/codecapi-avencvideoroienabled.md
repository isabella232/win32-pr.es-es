---
description: Indica si se respetará o no el atributo MFSampleExtension ROIRectangle establecido en el ejemplo de \_ entrada.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: CODECAPI_AVEncVideoROIEnabled propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269223"
---
# <a name="codecapi_avencvideoroienabled-property"></a>Propiedad CODECAPI \_ AVEncVideoROIEnabled

Indica si se respetará o no el atributo [ \_ MFSampleExtension ROIRectangle](mfsampleextension-roirectangle.md) establecido en el ejemplo de entrada.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Observaciones

El valor predeterminado es 0.

Si un MFT del codificador acepta un valor distinto de cero, se espera que el codificador respetará el atributo [ \_ MFSampleExtension ROIRectangle](mfsampleextension-roirectangle.md) establecido en el ejemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




