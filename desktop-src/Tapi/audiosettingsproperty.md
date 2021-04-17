---
description: 'Los métodos ITAudioSettings:: GetRange, ITAudioSettings:: get y ITAudioSettings:: set usan la enumeración AudioSettingsProperty para indicar la propiedad de configuración de audio que se está solucionando.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumeración AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690492"
---
# <a name="audiosettingsproperty-enumeration"></a>Enumeración AudioSettingsProperty

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Los métodos [**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings:: get**](itaudiosettings-get.md)y [**ITAudioSettings:: set**](itaudiosettings-set.md) usan la enumeración **AudioSettingsProperty** para indicar la propiedad de configuración de audio que se está solucionando.

## <a name="syntax"></a>Sintaxis


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Propiedad de configuración de la señal.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Propiedad de umbral de latencia.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volumen AudioSettings**
</dt> <dd>

Propiedad de volumen.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**\_Saldo de AudioSettings**
</dt> <dd>

Propiedad saldo.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_Sonoridad AudioSettings**
</dt> <dd>

Propiedad de sonoridad.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ agudos**
</dt> <dd>

Propiedad de agudos.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ graves**
</dt> <dd>

Propiedad Bass.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**\_Mono AudioSettings**
</dt> <dd>

Propiedad monoaural.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings:: get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings:: set**](itaudiosettings-set.md)
</dt> </dl>

 

 




