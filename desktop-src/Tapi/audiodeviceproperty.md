---
description: 'Los métodos ITAudioDeviceControl:: GetRange, ITAudioDeviceControl:: get y ITAudioDeviceControl:: set usan la enumeración AudioDeviceProperty para indicar la propiedad que se está solucionando.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumeración AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680324"
---
# <a name="audiodeviceproperty-enumeration"></a>Enumeración AudioDeviceProperty

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Los métodos [**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl:: get**](itaudiodevicecontrol-get.md)y [**ITAudioDeviceControl:: set**](itaudiodevicecontrol-set.md) usan la enumeración **AudioDeviceProperty** para indicar la propiedad que se está solucionando.

## <a name="syntax"></a>Sintaxis


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**
</dt> <dd>

Indica que se está configurando o recuperando el modo dúplex del dispositivo.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

Indica que se está configurando o recuperando el control de ganancia automática del dispositivo.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**
</dt> <dd>

Indica que se están configurando o recuperando las propiedades de cancelación del eco acústico del dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl:: get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl:: set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




