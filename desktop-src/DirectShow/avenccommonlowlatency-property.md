---
description: Especifica si el flujo de salida se debe estructurar para que la secuencia codificada tenga una latencia de descodificación baja.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propiedad AVEncCommonLowLatency (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274793"
---
# <a name="avenccommonlowlatency-property"></a>Propiedad AVEncCommonLowLatency

Especifica si el flujo de salida se debe estructurar para que la secuencia codificada tenga una latencia de descodificación baja.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Observaciones

La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer. Por ejemplo, si se establece esta propiedad en **Variant \_ true** en un codificador de vídeo MPEG, se limitan los tipos de estructuras GOP que el codificador puede utilizar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




