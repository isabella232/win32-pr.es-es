---
description: Habilita o deshabilita el relleno del altavoz en un descodificador de audio o en un procesador de señal digital (DSP).
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: Propiedad AVDSPSpeakerFill (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16bcdda053439b76c9445f2f9c866ee26afb4858
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659297"
---
# <a name="avdspspeakerfill-property"></a>Propiedad AVDSPSpeakerFill

Habilita o deshabilita el relleno del altavoz en un descodificador de audio o en un procesador de señal digital (DSP).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDSPSpeakerFill**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la enumeración [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) .

## <a name="remarks"></a>Observaciones

El relleno del altavoz es un proceso DSP que convierte audio mono o estéreo en audio multicanal.

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

 

 




