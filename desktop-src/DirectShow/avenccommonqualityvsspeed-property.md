---
description: Especifica el equilibrio entre la calidad y la velocidad de la codificación. Esta propiedad es válida en todos los modos de control de velocidad.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propiedad AVEncCommonQualityVsSpeed (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161986"
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



| Value | Descripción                      |
|-------|----------------------------------|
| 0     | Codificación más rápida y de menor calidad.  |
| 100   | Codificación más lenta y de mayor calidad. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




