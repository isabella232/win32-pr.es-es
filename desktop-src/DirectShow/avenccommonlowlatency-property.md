---
description: Especifica si el flujo de salida debe estructurarse para que la secuencia codificada tenga una latencia de descodificación baja.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propiedad AVEncCommonLowLatency (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b53c4b0122e595c930828f400600fc22b5a03977a781adab0e3a2f42b1048ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690235"
---
# <a name="avenccommonlowlatency-property"></a>Propiedad AVEncCommonLowLatency

Especifica si el flujo de salida debe estructurarse para que la secuencia codificada tenga una latencia de descodificación baja.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Comentarios

La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer. Por ejemplo, establecer esta propiedad en **VARIANT \_ TRUE** en un codificador de vídeo MPEG limita los tipos de estructuras GOP que el codificador puede usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




