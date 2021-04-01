---
title: Propiedad DeviceInstanceId de IMsRdpDevice
description: Recupera el identificador de instancia del dispositivo.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceInstanceId
- Propiedad DeviceInstanceId Servicios de Escritorio remoto, interfaz IMsRdpDevice
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice, propiedad DeviceInstanceId
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
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997147"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a>IMsRdpDevice::D propiedad eviceInstanceId

Recupera el identificador de instancia del dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a>Valor de propiedad

Identificador de instancia del dispositivo.

## <a name="error-codes"></a>Códigos de error

Si el método se ejecuta correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





