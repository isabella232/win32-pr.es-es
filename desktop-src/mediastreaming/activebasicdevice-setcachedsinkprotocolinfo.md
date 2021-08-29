---
title: Método ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice.h)
description: Obtiene la información del protocolo de receptor almacenado en caché para el dispositivo. | Método ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice.h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- Método SetCachedSinkProtocolInfo de Media Streaming API
- Método SetCachedSinkProtocolInfo de Media Streaming API , interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API, método SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcfc780371f339b4fd14620975fc27e8dd08ed6ac9f054cfd2654840dc8022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952765"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a>Método ActiveBasicDevice::SetCachedSinkProtocolInfo

Obtiene la información del protocolo de receptor almacenado en caché para el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*physicalNetworkInterface* \[ En\]
</dt> <dd>

Especifica la interfaz de red física.

</dd> <dt>

*velocidad de bits* \[ En\]
</dt> <dd>

Valor de velocidad de bits.

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

 

