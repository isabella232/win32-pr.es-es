---
description: La enumeración AudioSettingsProperty la usan los métodos ITAudioSettings::GetRange, ITAudioSettings::Get e ITAudioSettings::Set para indicar la propiedad de configuración de audio que se está abordando.
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumeración AudioSettingsProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b15cfb5a0211f02ac333ba75e47b5e4cbd5c44865b4a18c2f19ea3a8769dde3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871535"
---
# <a name="audiosettingsproperty-enumeration"></a>Enumeración AudioSettingsProperty

\[Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **enumeración AudioSettingsProperty** la usan los métodos [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md)e [**ITAudioSettings::Set**](itaudiosettings-set.md) para indicar la propiedad de configuración de audio que se está abordando.

## <a name="syntax"></a>Syntax


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Propiedad de configuración de señal.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Propiedad umbral de silencio.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**Volumen \_ AudioSettings**
</dt> <dd>

Propiedad Volume.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ Balance**
</dt> <dd>

Propiedad Balance.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings \_ Loudness**
</dt> <dd>

Propiedad Sonoridad.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ Treble**
</dt> <dd>

Propiedad treble.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Graver**
</dt> <dd>

Propiedad Debajo.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ Mono**
</dt> <dd>

Propiedad Dementeural.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings::Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings::Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




