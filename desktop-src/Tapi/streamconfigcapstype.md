---
description: La estructura de la configuración de la secuencia de TAPI usa el tipo de enumeración StreamConfigCapsType \_ \_ \_ para indicar si está implicado el streaming de audio o vídeo.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Enumeración StreamConfigCapsType (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681277"
---
# <a name="streamconfigcapstype-enumeration"></a>Enumeración StreamConfigCapsType

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La estructura de la configuración de la [**secuencia de \_ TAPI \_ \_**](tapi-stream-config-caps.md) usa el tipo de enumeración **StreamConfigCapsType** para indicar si está implicado el streaming de audio o vídeo.

## <a name="syntax"></a>Sintaxis


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**
</dt> <dd>

Configuración de transmisión por secuencias de audio.

</dd> <dt>

<span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**
</dt> <dd>

Configuración de streaming de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Cap de \_ configuración de secuencia TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




