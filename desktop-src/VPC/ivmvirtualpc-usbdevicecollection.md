---
title: Propiedad IVMVirtualPC USBDeviceCollection (VPCCOMInterfaces.h)
description: Colección enumerable de todos los dispositivos USB conectados al host.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- USBDeviceCollection, propiedad Virtual PC
- Propiedad USBDeviceCollection De PC virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , PROPIEDAD USBDeviceCollection
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2880a6f7adb60605e37fe78481613016d17fdbbd2e27f1a6add4ce031030deea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136528"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a>IVMVirtualPC::USBDeviceCollection, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una colección enumerable de todos los dispositivos USB conectados al host.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Valor de propiedad

Referencia a un [**puntero IVMUSBDeviceCollection**](ivmusbdevicecollection.md) que representa una colección de [**objetos IVMUSBDevice.**](ivmusbdevice.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                                | Significado                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                                   | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                     | El parámetro es **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                             | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E ERROR \_ DE ENUMERACIÓN USB \_ MÁS \_ \_ \_ DISPOSITIVOS</dt> <dt>0XA0040930</dt> </dl> | Hay más de 16 dispositivos USB conectados al host.<br/>                                  |
| <dl> <dt>Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA</dt> <dt>0xA0040951</dt> </dl>      | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

