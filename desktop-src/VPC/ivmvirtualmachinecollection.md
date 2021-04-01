---
title: Interfaz IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Define la colección de máquinas virtuales dentro de Windows Virtual PC. Para obtener un objeto IVMVirtualMachineCollection, use la propiedad VirtualMachines de IVMVirtualPC.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Interfaz IVMVirtualMachineCollection Virtual PC
- Interfaz IVMVirtualMachineCollection Virtual PC, descripción
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
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150941"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Interfaz IVMVirtualMachineCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de máquinas virtuales dentro de Windows Virtual PC. Para obtener un objeto **IVMVirtualMachineCollection** , use la propiedad [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Miembros

La interfaz **IVMVirtualMachineCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMVirtualMachineCollection** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                   |
| [**Contabiliza**](ivmvirtualmachinecollection-count.md)<br/>        | Solo lectura<br/> | El número de máquinas virtuales de esta colección.<br/>                  |
| [**Elemento**](ivmvirtualmachinecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de máquina virtual que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection se define como 59f31786-2a3d-4fbf-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

