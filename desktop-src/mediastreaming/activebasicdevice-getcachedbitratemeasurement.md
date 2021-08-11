---
title: Método ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice.h)
description: Obtiene la velocidad de bits almacenada en caché.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- Método GetCachedBitrateMeasurement de Media Streaming API
- Método GetCachedBitrateMeasurement Media Streaming API, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API, método GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 031d77595298651be11c793f8fd96471808ab1aef3f5a2b6398be9c1ff10de02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236870"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>Método ActiveBasicDevice::GetCachedBitrateMeasurement

Obtiene la velocidad de bits almacenada en caché.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*physicalNetworkInterface* \[ En\]
</dt> <dd>

Especifica la interfaz de red física.

</dd> <dt>

*velocidad de bits* \[ out, retval\]
</dt> <dd>

Recibe el valor de velocidad de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

