---
title: Método ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice.h)
description: Obtiene el ancho de banda efectivo actual del dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- Método GetEffectiveBandwidth de Media Streaming API
- Método GetEffectiveBandwidth de Media Streaming API, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API, método GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236787"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Método ActiveBasicDevice::GetEffectiveBandwidth

Obtiene el ancho de banda efectivo actual del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*transmitSpeed* \[ in, retval\]
</dt> <dd>

Especifica si se recupera la velocidad de transmisión o se recupera la velocidad de recepción.

**True** para recuperar la velocidad de transmisión. **false** para recuperar la velocidad de recepción.

</dd> <dt>

*currentSpeed* \[ out\]
</dt> <dd>

Recibe el ancho de banda efectivo actual.

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

 

