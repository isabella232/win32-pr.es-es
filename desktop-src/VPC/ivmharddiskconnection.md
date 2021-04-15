---
title: Interfaz IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Define la conexión para un disco duro dentro de la máquina virtual.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Interfaz IVMHardDiskConnection Virtual PC
- Interfaz IVMHardDiskConnection Virtual PC, descripción
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
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695964"
---
# <a name="ivmharddiskconnection-interface"></a>Interfaz IVMHardDiskConnection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la conexión para un disco duro dentro de la máquina virtual. El método [**IVMVirtualMachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) devuelve un objeto **IVMHardDiskConnection** . También puede recuperar un objeto **IVMHardDiskConnection** del objeto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) devuelto desde la propiedad [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Miembros

La interfaz **IVMHardDiskConnection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnection** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMHardDiskConnection** tiene estos métodos.



| Método                                                         | Descripción                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | Establece la ubicación del bus al que está conectado este disco duro.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMHardDiskConnection** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso          | Descripción                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | Solo lectura<br/> | Número de bus al que está conectada la imagen de la unidad.<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | Solo lectura<br/> | El número de dispositivo al que está conectada la imagen de la unidad.<br/>                |
| [**Detectar**](ivmharddiskconnection-harddisk.md)<br/>         | Solo lectura<br/> | Un objeto de disco duro correspondiente a esta conexión.<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Solo lectura<br/> | Un objeto de disco duro correspondiente a la imagen de disco para deshacer de esta conexión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



 

