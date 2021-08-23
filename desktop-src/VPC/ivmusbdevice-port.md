---
title: Propiedad IVMUSBDevice Port (VPCCOMInterfaces.h)
description: Recupera el identificador del puerto en el que está conectado el dispositivo.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Propiedad de puerto Virtual PC
- Propiedad de puerto Virtual PC, interfaz IVMUSBDevice
- INTERFAZ IVMUSBDispositivo Pc virtual, propiedad Puerto
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5b564f1e8c75ecbf5bb140d17218df83bc5b23f5de219c819dc5c4f31f7be14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998715"
---
# <a name="ivmusbdeviceport-property"></a>IVMUSBDevice::P ort

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el identificador del puerto en el que está conectado el dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a>Valor de propiedad

Identificador de puerto. El controlador del conector USB asigna este valor.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                            | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>               | El método se completó correctamente.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl> | El parámetro es **NULL.**<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMUSBDevice se define como \_ 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

