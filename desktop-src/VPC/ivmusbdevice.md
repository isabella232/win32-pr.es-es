---
title: Interfaz IVMUSBDevice (VPCCOMInterfaces. h)
description: Define la interfaz para un dispositivo USB conectado al host. Puede conectar el dispositivo USB a una máquina virtual para usar el dispositivo dentro de la máquina virtual.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Interfaz IVMUSBDevice Virtual PC
- Interfaz IVMUSBDevice Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695950"
---
# <a name="ivmusbdevice-interface"></a>Interfaz IVMUSBDevice

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la interfaz para un dispositivo USB conectado al host. Puede conectar el dispositivo USB a una máquina virtual para usar el dispositivo dentro de la máquina virtual.

## <a name="members"></a>Miembros

La interfaz **IVMUSBDevice** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDevice** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMUSBDevice** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso          | Descripción                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**AttachedToVM**](ivmusbdevice-attachedtovm.md)<br/>             | Solo lectura<br/> | El nombre de la máquina virtual a la que está conectado el dispositivo USB.<br/> |
| [**DeviceClass**](ivmusbdevice-deviceclass.md)<br/>               | Solo lectura<br/> | La clase de dispositivo del dispositivo USB.<br/>                                  |
| [**DeviceString**](ivmusbdevice-devicestring.md)<br/>             | Solo lectura<br/> | Nombre del dispositivo USB.<br/>                                          |
| [**HubID**](ivmusbdevice-hubid.md)<br/>                           | Solo lectura<br/> | Identificador del concentrador en el que está conectado el dispositivo.<br/>          |
| [**ManufacturerString**](ivmusbdevice-manufacturerstring.md)<br/> | Solo lectura<br/> | Nombre del fabricante del dispositivo USB.<br/>                             |
| [**Port**](ivmusbdevice-port.md)<br/>                             | Solo lectura<br/> | El identificador del puerto en el que está conectado el dispositivo.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



 

