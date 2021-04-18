---
description: El método GetRange recupera el intervalo de valores válidos para una propiedad de dispositivo de audio determinada.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'ITAudioDeviceControl:: GetRange (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679113"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>ITAudioDeviceControl:: GetRange (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetRange** recupera el intervalo de valores válidos para una [**propiedad de dispositivo de audio**](audiodeviceproperty.md)determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ de\]
</dt> <dd>

Miembro de la enumeración [**AudioDeviceProperty**](audiodeviceproperty.md) .

</dd> <dt>

*plMin* \[ enuncia\]
</dt> <dd>

Valor mínimo válido para la propiedad de entrada.

</dd> <dt>

*plMax* \[ enuncia\]
</dt> <dd>

Valor máximo válido para la propiedad de entrada.

</dd> <dt>

*plSteppingDelta* \[ enuncia\]
</dt> <dd>

Incremento por el que se puede aumentar o disminuir el valor de la propiedad.

</dd> <dt>

*plDefault* \[ enuncia\]
</dt> <dd>

Valor predeterminado del parámetro *Property* .

</dd> <dt>

*plFlags* \[ enuncia\]
</dt> <dd>

Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




