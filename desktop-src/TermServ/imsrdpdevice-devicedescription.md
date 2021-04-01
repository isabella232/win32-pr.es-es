---
title: Propiedad DeviceDescription de IMsRdpDevice
description: Recupera la descripción del dispositivo que se va a mostrar al usuario si el nombre para mostrar no está disponible.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceDescription
- Propiedad DeviceDescription Servicios de Escritorio remoto, interfaz IMsRdpDevice
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice, propiedad DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150597"
---
# <a name="imsrdpdevicedevicedescription-property"></a>IMsRdpDevice::D propiedad eviceDescription

Recupera la descripción del dispositivo que se va a mostrar al usuario si el nombre para mostrar no está disponible.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a>Valor de propiedad

Descripción del dispositivo.

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

 

 





