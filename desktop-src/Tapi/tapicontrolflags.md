---
description: Varios métodos usan la enumeración TAPIControlFlags para indicar si una propiedad determinada se controla de forma automática o manual.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumeración TAPIControlFlags (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278cc2328335409d4ffcc95ea136826d121acd57776f98aaad947c8fb9ee5d93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139808"
---
# <a name="tapicontrolflags-enumeration"></a>TAPIControlFlags (enumeración)

\[Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Varios métodos usan la enumeración **TAPIControlFlags** para indicar si una propiedad determinada se controla de forma automática o manual.

## <a name="syntax"></a>Syntax


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**Marcas TAPIControl \_ \_ None**
</dt> <dd>

TAPI no tiene marcas de control para la propiedad .

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**MARCAS TAPIControl \_ \_ Auto**
</dt> <dd>

La propiedad se controla automáticamente.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**Manual de marcas \_ TAPIControl \_**
</dt> <dd>

La propiedad se controla manualmente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md)
</dt> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings::Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings::Set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl::Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl::Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




