---
title: Método ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Obtiene el ancho de banda efectivo actual para el dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- Método GetEffectiveBandwidth API de streaming de multimedia
- Método GetEffectiveBandwidth API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método GetEffectiveBandwidth
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
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079723"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>ActiveBasicDevice:: GetEffectiveBandwidth (método)

Obtiene el ancho de banda efectivo actual para el dispositivo.

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

**true** para recuperar la velocidad de transmisión. **false** para recuperar la velocidad de recepción.

</dd> <dt>

*currentSpeed* \[ enuncia\]
</dt> <dd>

Recibe el ancho de banda efectivo actual.

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

 

