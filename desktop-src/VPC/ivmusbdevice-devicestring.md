---
title: Propiedad IVMUSBDevice DeviceString (VPCCOMInterfaces.h)
description: Recupera el nombre del dispositivo USB.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- DeviceString, propiedad Virtual PC
- Propiedad DeviceString Virtual PC, interfaz IVMUSBDevice
- INTERFAZ IVMUSBDispositivo Pc virtual, propiedad DeviceString
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efab8af122c0411ffaaca23302893ef2b354611e5c2d24fbd30e17eaa4782e8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752564"
---
# <a name="ivmusbdevicedevicestring-property"></a>IVMUSBDevice::D eviceString

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el nombre del dispositivo USB.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del dispositivo USB.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                            | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>               | El método se completó correctamente.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl> | El parámetro es **NULL.**<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMUSBDevice se define como \_ 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

