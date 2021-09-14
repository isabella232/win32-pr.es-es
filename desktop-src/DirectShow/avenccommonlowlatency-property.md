---
description: Especifica si el flujo de salida se debe estructurar para que el flujo codificado tenga una latencia de descodificación baja.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propiedad AVEncCommonLowLatency (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162025"
---
# <a name="avenccommonlowlatency-property"></a>Propiedad AVEncCommonLowLatency

Especifica si el flujo de salida se debe estructurar para que el flujo codificado tenga una latencia de descodificación baja.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Observaciones

La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer. Por ejemplo, si se establece esta propiedad en **VARIANT \_ TRUE** en un codificador de vídeo MPEG, se limitan los tipos de estructuras GOP que puede usar el codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio aplicaciones para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




