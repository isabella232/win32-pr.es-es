---
title: Propiedad IVMUSBDevice DeviceClass (VPCCOMInterfaces.h)
description: Recupera la clase de dispositivo del dispositivo USB.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- DeviceClass, propiedad Virtual PC
- Propiedad DeviceClass Virtual PC , interfaz IVMUSBDevice
- INTERFAZ IVMUSBDispositivo Pc virtual, propiedad DeviceClass
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f192c81e8dff1d0b1f124393c9eceb9f6268ac43043337399dedb9cdcbebb3be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006915"
---
# <a name="ivmusbdevicedeviceclass-property"></a>Propiedad IVMUSBDevice::D eviceClass

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la clase de dispositivo del dispositivo USB.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a>Valor de propiedad

Clase de dispositivo. Para obtener una lista de valores, [**vea VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                            | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>               | El método se completó correctamente.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl> | El parámetro es **NULL.**<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMUSBDevice se define como \_ 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

