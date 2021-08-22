---
title: IMsRdpDevice DeviceInstanceId, propiedad
description: Recupera el identificador de instancia de dispositivo del dispositivo.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Propiedad DeviceInstanceId Servicios de Escritorio remoto
- Propiedad DeviceInstanceId Servicios de Escritorio remoto , interfaz IMsRdpDevice
- Interfaz IMsRdpDevice Servicios de Escritorio remoto , propiedad DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fd93b775d3fd239435a984cf0f0b7518558f3f57e92525365764da580f499c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606821"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a>Propiedad IMsRdpDevice::D eviceInstanceId

Recupera el identificador de instancia de dispositivo del dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a>Valor de propiedad

Identificador de la instancia del dispositivo.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDevice se define como \_ 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





