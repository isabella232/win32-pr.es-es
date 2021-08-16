---
title: Interfaz IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
description: Define la colección de conexiones de disco duro dentro de la máquina virtual. Para obtener un objeto IVMHardDiskConnectionCollection, use la propiedad IVMVirtualMachine HardDiskConnections.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- IVMHardDiskConnectionCollection interface Virtual PC
- IVMHardDiskConnectionCollection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997cbe915e7e4addac60c639a7ee6c260f07271ff5981939b25dbefd49fcba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345709"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>IVMHardDiskConnectionCollection (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la colección de conexiones de disco duro dentro de la máquina virtual. Para obtener un **objeto IVMHardDiskConnectionCollection,** use la [**propiedad IVMVirtualMachine::HardDiskConnections.**](ivmvirtualmachine-harddiskconnections.md)

## <a name="members"></a>Miembros

La **interfaz IVMHardDiskConnectionCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDiskConnectionCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMHardDiskConnectionCollection** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso          | Descripción                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                        |
| [**Contar**](ivmharddiskconnectioncollection-count.md)<br/>        | Solo lectura<br/> | Número de conexiones de disco duro de esta colección.<br/>                  |
| [**Elemento**](ivmharddiskconnectioncollection-item.md)<br/>          | Solo lectura<br/> | Objeto de conexión de disco duro que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                               |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID IVMHardDiskconnectionCollection se define como \_ b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

