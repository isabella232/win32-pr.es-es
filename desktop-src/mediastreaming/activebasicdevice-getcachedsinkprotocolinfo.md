---
title: Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtiene la información del protocolo del receptor almacenado en caché para el dispositivo. | Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- Método GetCachedSinkProtocolInfo API de streaming de multimedia
- Método GetCachedSinkProtocolInfo API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método GetCachedSinkProtocolInfo
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
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698134"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>ActiveBasicDevice:: GetCachedSinkProtocolInfo (método)

Obtiene la información del protocolo del receptor almacenado en caché para el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de out, retval\]
</dt> <dd>

Información del protocolo receptor en caché para el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

