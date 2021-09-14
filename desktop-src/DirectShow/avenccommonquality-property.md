---
description: Especifica el nivel de calidad para la codificación.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propiedad AVEncCommonQuality (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161990"
---
# <a name="avenccommonquality-property"></a>Propiedad AVEncCommonQuality

Especifica el nivel de calidad para la codificación.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Value | Descripción                           |
|-------|---------------------------------------|
| 0     | Calidad mínima, tamaño de salida más pequeño. |
| 100   | Calidad máxima, tamaño de salida mayor.  |



 

## <a name="remarks"></a>Observaciones

Esta propiedad controla el nivel de calidad cuando el codificador no usa una velocidad de bits restringida. La [**propiedad AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina si la velocidad de bits está restringida.

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

 

 




