---
title: Interfaz IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Define la colección de conexiones de disco duro dentro de la máquina virtual. Para obtener un objeto IVMHardDiskConnectionCollection, use la propiedad HardDiskConnections de IVMVirtualMachine.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Interfaz IVMHardDiskConnectionCollection Virtual PC
- Interfaz IVMHardDiskConnectionCollection Virtual PC, descripción
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
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488926"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Interfaz IVMHardDiskConnectionCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de conexiones de disco duro dentro de la máquina virtual. Para obtener un objeto **IVMHardDiskConnectionCollection** , use la propiedad [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Miembros

La interfaz **IVMHardDiskConnectionCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnectionCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMHardDiskConnectionCollection** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso          | Descripción                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                        |
| [**Contabiliza**](ivmharddiskconnectioncollection-count.md)<br/>        | Solo lectura<br/> | El número de conexiones de disco duro en esta colección.<br/>                  |
| [**Elemento**](ivmharddiskconnectioncollection-item.md)<br/>          | Solo lectura<br/> | Objeto de conexión del disco duro que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                               |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection se define como b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

