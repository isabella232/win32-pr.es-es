---
title: Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice.h)
description: Obtiene la información del protocolo de receptor almacenado en caché para el dispositivo. | Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice.h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- Método GetCachedSinkProtocolInfo de Media Streaming API
- Método GetCachedSinkProtocolInfo de Media Streaming API, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API, método GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a9ebda71f59dc4bd887479b5ff9e763844b32985736f8cf224ed4981f04b34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736401"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>Método ActiveBasicDevice::GetCachedSinkProtocolInfo

Obtiene la información del protocolo de receptor almacenado en caché para el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Información del protocolo de receptor almacenado en caché para el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

