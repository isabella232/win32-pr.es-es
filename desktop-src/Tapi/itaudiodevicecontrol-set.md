---
description: El método Set establece el valor de una propiedad de dispositivo de audio determinada.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: ItAudioDeviceControl::Set (Método, Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6fc99d5f6084ff2d5d2226847a395a21c3dcaeb6156d769c768768f10d186c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775045"
---
# <a name="itaudiodevicecontrolset-method"></a>ITAudioDeviceControl::Set (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Set** establece el valor de una propiedad de dispositivo de audio [**determinada.**](audiodeviceproperty.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ En\]
</dt> <dd>

Miembro de la [**enumeración AudioDeviceProperty.**](audiodeviceproperty.md)

</dd> <dt>

*lValue* \[ En\]
</dt> <dd>

Valor deseado para la propiedad.

</dd> <dt>

*lFlags* \[ En\]
</dt> <dd>

Valor de la [**enumeración TAPIControlFlags**](tapicontrolflags.md) que indica cómo *se* va a controlar el valor property.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




