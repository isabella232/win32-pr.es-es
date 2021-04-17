---
description: Controla la señalización de MFSampleExtension \_ MeanAbsoluteDifference a través de IMFAttribute en cada ejemplo de salida.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Propiedad CODECAPI_AVEncVideoMeanAbsoluteDifference (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696171"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>\_Propiedad AVEncVideoMeanAbsoluteDifference de CODECAPI

Controla la señalización de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a través de [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en cada ejemplo de salida.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**

## <a name="remarks"></a>Observaciones

Si la aplicación establece un valor distinto de cero, el codificador debería agregar el atributo de ejemplo [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a cada ejemplo de salida. El \_ atributo MeanAbsoluteDifference de MFSampleExtension indica la diferencia absoluta media entre los ejemplos de origen y los ejemplos de predicción en el plano y.

Si el codificador devuelve 0 para **GetParameterRange**, el codificador no admite la salida de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) en los ejemplos de salida.

El valor predeterminado debe ser 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




