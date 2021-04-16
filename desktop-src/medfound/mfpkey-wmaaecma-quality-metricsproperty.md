---
description: Recupera las métricas de calidad de la cancelación de eco acústico (AEC) del DSP de captura de voz.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: Propiedad MFPKEY_WMAAECMA_QUALITY_METRICS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696691"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>\_Propiedad de \_ \_ métricas de calidad de MFPKEY WMAAECMA

Recupera las métricas de calidad de la cancelación de eco acústico (AEC) del DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

BLOB de VT \_

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es una estructura de [ \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) . Esta propiedad es de solo lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
