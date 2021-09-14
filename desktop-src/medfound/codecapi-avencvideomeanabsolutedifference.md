---
description: Controla la señalización de MFSampleExtension \_ MeanAbsoluteDifference a través deATTRIBUTEAttribute en cada ejemplo de salida.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: CODECAPI_AVEncVideoMeanAbsoluteDifference propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269255"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>Propiedad CODECAPI \_ AVEncVideoMeanAbsoluteDifference

Controla la señalización de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a través [**deATTRIBUTEAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en cada ejemplo de salida.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**

## <a name="remarks"></a>Observaciones

Si la aplicación establece un valor distinto de cero, el codificador debe agregar el atributo de ejemplo [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a cada ejemplo de salida. El atributo MFSampleExtension MeanAbsoluteDifference indica la diferencia absoluta media entre las muestras de origen y las muestras predichos \_ en el plano Y.

Si el codificador devuelve 0 para **GetParameterRange**, el codificador no admite la salida de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) en los ejemplos de salida.

El valor predeterminado debe ser 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




