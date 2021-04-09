---
description: Obtiene la configuración de los altavoces para los canales de audio en el flujo de bits de audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propiedad AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079952"
---
# <a name="avaudiochannelconfig-property"></a>Propiedad AVAudioChannelConfig

Obtiene la configuración de los altavoces para los canales de audio en el flujo de bits de audio.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es una operación OR bit a bit de los miembros de la enumeración [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .

## <a name="remarks"></a>Observaciones

El número de canales incluye el canal de efecto de baja frecuencia (LFE), si está presente.

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

 

 




