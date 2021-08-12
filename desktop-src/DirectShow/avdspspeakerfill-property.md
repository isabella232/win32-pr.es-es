---
description: Habilita o deshabilita el relleno del altavoz en un descodificador de audio o un procesador de señales digitales (DSP).
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: Propiedad AVDSPSpeakerFill (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff4886f1b6f1e6ae19f9f1b5bf78e20159df390f2d642ac2b9cb3c4c834d1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663436"
---
# <a name="avdspspeakerfill-property"></a>Propiedad AVDSPSpeakerFill

Habilita o deshabilita el relleno del altavoz en un descodificador de audio o un procesador de señales digitales (DSP).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDSPSpeakerFill**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDSPSpeakerFill.**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)

## <a name="remarks"></a>Observaciones

El relleno del altavoz es un proceso de DSP que convierte el audio mono o estéreo en audio multicanal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




