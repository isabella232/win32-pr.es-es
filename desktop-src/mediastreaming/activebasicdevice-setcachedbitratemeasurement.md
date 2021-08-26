---
title: Método ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice.h)
description: Establece la velocidad de bits almacenada en caché.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Método SetCachedBitrateMeasurement de Media Streaming API
- Método SetCachedBitrateMeasurement Media Streaming API , interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API, método SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf79b7e9066aacfcce1f82c998463d6d620f5061fef4af788104a0c01a44ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952776"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Método ActiveBasicDevice::SetCachedBitrateMeasurement

Establece la velocidad de bits almacenada en caché.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCachedBitrateMeasurement(
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

Valor en el que se establece la velocidad de bits.

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

 

