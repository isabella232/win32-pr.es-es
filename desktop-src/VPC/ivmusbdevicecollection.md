---
title: Interfaz IVMUSBDeviceCollection (VPCCOMInterfaces.h)
description: Define la colección de dispositivos USB conectados al sistema host. Para obtener un objeto IVMUSBDeviceCollection, use la propiedad IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- PC virtual de la interfaz IVMUSBDeviceCollection
- IvMUSBDeviceCollection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752544"
---
# <a name="ivmusbdevicecollection-interface"></a>Interfaz IVMUSBDeviceCollection

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la colección de dispositivos USB conectados al sistema host. Para obtener un **objeto IVMUSBDeviceCollection,** use la [**propiedad IVMVirtualPC::USBDeviceCollection.**](ivmvirtualpc-usbdevicecollection.md)

## <a name="members"></a>Miembros

La **interfaz IVMUSBDeviceCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMUSBDeviceCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMUSBDeviceCollection** tiene estas propiedades.



| Propiedad                                                        | Tipo de acceso          | Descripción                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                        |
| [**Contar**](ivmusbdevicecollection-count.md)<br/>        | Solo lectura<br/> | Número de dispositivos USB de esta colección.<br/>                            |
| [**Elemento**](ivmusbdevicecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de dispositivo USB que corresponde al índice especificado (basado en 1).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMUSBDeviceCollection se define como \_ 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

