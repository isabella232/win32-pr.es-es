---
description: Especifica el equilibrio entre la calidad y la velocidad de la codificación. Esta propiedad es válida en todos los modos de control de velocidad.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propiedad AVEncCommonQualityVsSpeed (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9def8fc53a6cf88384a42870ef695294a0117ab3bfdd26ba69c95bd2b02a63b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540885"
---
# <a name="avenccommonqualityvsspeed-property"></a>Propiedad AVEncCommonQualityVsSpeed

Especifica el equilibrio entre la calidad y la velocidad de la codificación. Esta propiedad es válida en todos los modos de control de velocidad.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Valor | Descripción                      |
|-------|----------------------------------|
| 0     | Codificación más rápida y de menor calidad.  |
| 100   | Codificación más lenta y de mayor calidad. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




