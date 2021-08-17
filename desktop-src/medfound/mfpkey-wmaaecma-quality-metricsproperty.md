---
description: Recupera métricas de calidad sobre la cancelación de eco acústico (AEC) del DSP de captura de voz.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: MFPKEY_WMAAECMA_QUALITY_METRICS propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2186876279ee45e34444866c206a7729c0674c8dff1bc57c255ca205e911edae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689270"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ QUALITY \_ METRICS

Recupera métricas de calidad sobre la cancelación de eco acústico (AEC) del DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BLOB

## <a name="remarks"></a>Comentarios

El valor de esta propiedad es una [estructura \_ Struct AecQualityMetrics.](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) Esta propiedad es de solo lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
