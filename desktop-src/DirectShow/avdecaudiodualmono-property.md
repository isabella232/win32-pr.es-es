---
description: Especifica si el audio de 2 canales se codifica como estéreo o dual mono.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propiedad AVDecAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906771"
---
# <a name="avdecaudiodualmono-property"></a>Propiedad AVDecAudioDualMono

Especifica si el audio de 2 canales se codifica como estéreo o dual mono.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la enumeración [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .

## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica cuando el flujo de bits de entrada del descodificador contiene audio de dos canales. Una secuencia de audio de dos canales podría estar codificada como estéreo o como dual mono. Si el audio es dual mono, puede establecer la propiedad [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) para configurar el modo en que el descodificador reproduce el audio.

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

 

 




