---
title: Interfaz IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Define la colección de dispositivos USB conectados al sistema host. Para obtener un objeto IVMUSBDeviceCollection, use la propiedad USBDeviceCollection de IVMVirtualPC.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Interfaz IVMUSBDeviceCollection Virtual PC
- Interfaz IVMUSBDeviceCollection Virtual PC, descripción
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
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695930"
---
# <a name="ivmusbdevicecollection-interface"></a>Interfaz IVMUSBDeviceCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de dispositivos USB conectados al sistema host. Para obtener un objeto **IVMUSBDeviceCollection** , use la propiedad [**IVMVirtualPC:: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .

## <a name="members"></a>Miembros

La interfaz **IVMUSBDeviceCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDeviceCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMUSBDeviceCollection** tiene estas propiedades.



| Propiedad                                                        | Tipo de acceso          | Descripción                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                        |
| [**Contabiliza**](ivmusbdevicecollection-count.md)<br/>        | Solo lectura<br/> | El número de dispositivos USB en esta recopilación.<br/>                            |
| [**Elemento**](ivmusbdevicecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de dispositivo USB que corresponde al índice especificado (basado en 1).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection se define como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

