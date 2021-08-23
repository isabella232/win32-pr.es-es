---
title: Interfaz IVMHardDiskConnection (VPCCOMInterfaces.h)
description: Define la conexión de un disco duro dentro de la máquina virtual.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- IVMHardDiskConnection interface Virtual PC
- IVMHardDiskConnection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8522a6f8c24f2f80728a878435b42ac4179432e1cca4234feb29261fe2c11f8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510795"
---
# <a name="ivmharddiskconnection-interface"></a>Interfaz IVMHardDiskConnection

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la conexión de un disco duro dentro de la máquina virtual. Se **devuelve un objeto IVMHardDiskConnection** desde el método [**IVMVirtualMachine::AddHardDiskConnection.**](ivmvirtualmachine-addharddiskconnection.md) También puede recuperar un objeto **IVMHardDiskConnection** del objeto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) devuelto desde la [**propiedad IVMVirtualMachine::HardDiskConnections.**](ivmvirtualmachine-harddiskconnections.md)

## <a name="members"></a>Miembros

La **interfaz IVMHardDiskConnection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDiskConnection** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMHardDiskConnection** tiene estos métodos.



| Método                                                         | Descripción                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | Establece la ubicación del bus a la que está conectado este disco duro.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMHardDiskConnection** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso          | Descripción                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | Solo lectura<br/> | Número de bus al que está conectada la imagen de unidad.<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | Solo lectura<br/> | Número de dispositivo al que está conectada la imagen de unidad.<br/>                |
| [**Disco**](ivmharddiskconnection-harddisk.md)<br/>         | Solo lectura<br/> | Objeto de disco duro correspondiente a esta conexión.<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Solo lectura<br/> | Objeto de disco duro correspondiente a la imagen de deshacer disco de esta conexión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDiskconnection se define como \_ aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



 

