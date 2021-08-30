---
title: Interfaz IVMVirtualMachineCollection (VPCCOMInterfaces.h)
description: Define la colección de máquinas virtuales en Windows Virtual PC. Para obtener un objeto IVMVirtualMachineCollection, use la propiedad IVMVirtualPC VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- IVMVirtualMachineCollection interface Virtual PC
- Interfaz IVMVirtualMachineCollection Pc virtual , descrito
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ca6a04d95d20a6e18e5fe70b285becc6fb1744e1465dad4e20d0c28d9fa45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006795"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Interfaz IVMVirtualMachineCollection

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la colección de máquinas virtuales en Windows Virtual PC. Para obtener un **objeto IVMVirtualMachineCollection,** use la [**propiedad IVMVirtualPC::VirtualMachines.**](ivmvirtualpc-virtualmachines.md)

## <a name="members"></a>Miembros

La **interfaz IVMVirtualMachineCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualMachineCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMVirtualMachineCollection** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                   |
| [**Contar**](ivmvirtualmachinecollection-count.md)<br/>        | Solo lectura<br/> | Número de máquinas virtuales de esta colección.<br/>                  |
| [**Elemento**](ivmvirtualmachinecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de máquina virtual que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection se define como 59f31786-2a3d-4fbf-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

