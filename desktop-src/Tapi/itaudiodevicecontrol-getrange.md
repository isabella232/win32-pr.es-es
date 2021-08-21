---
description: El método GetRange recupera el intervalo de valores válidos para una propiedad de dispositivo de audio determinada.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: Método ITAudioDeviceControl::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87779131dea5bb01a1575074e4f019dbfa2a62addebf5b91a7eee6e9cc041710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003453"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>ItAudioDeviceControl::GetRange (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método GetRange** recupera el intervalo de valores válidos para una propiedad de [**dispositivo de audio determinada.**](audiodeviceproperty.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ En\]
</dt> <dd>

Miembro de la [**enumeración AudioDeviceProperty.**](audiodeviceproperty.md)

</dd> <dt>

*plMin* \[ out\]
</dt> <dd>

Valor mínimo válido para la propiedad de entrada.

</dd> <dt>

*plMax* \[ out\]
</dt> <dd>

Valor máximo válido para la propiedad de entrada.

</dd> <dt>

*plSteppingDelta* \[ out\]
</dt> <dd>

Incremento en el que se puede aumentar o disminuir el valor de la propiedad.

</dd> <dt>

*plDefault* \[ out\]
</dt> <dd>

Valor predeterminado para el *parámetro Property.*

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Valor de la [**enumeración TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el *valor* property.

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

 

 




