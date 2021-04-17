---
description: Una serie de métodos utiliza la enumeración TAPIControlFlags para indicar si una propiedad determinada se controla de forma automática o manual.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumeración TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690803"
---
# <a name="tapicontrolflags-enumeration"></a>Enumeración TAPIControlFlags

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Una serie de métodos utiliza la enumeración **TAPIControlFlags** para indicar si una propiedad determinada se controla de forma automática o manual.

## <a name="syntax"></a>Sintaxis


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ marca \_ ninguno**
</dt> <dd>

TAPI no tiene marcas de control para la propiedad.

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl \_ marcas \_ automáticas**
</dt> <dd>

La propiedad se controla automáticamente.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manual de marcas TAPIControl \_**
</dt> <dd>

La propiedad se controla manualmente.

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
</dt> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings:: get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings:: set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl:: get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl:: set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl:: get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




