---
title: Interfaz IVMFstonepyDriveCollection (VPCCOMInterfaces.h)
description: Define una colección de disquetes dentro de la máquina virtual.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- IVMFstonepyDriveCollection interface Virtual PC
- Interfaz IVMFstonepyDriveCollection Pc virtual , descrito
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6637c0c4a8c8b87f4458081b0893b0939c8eaf04c97738c02d39da5e0fd8eebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653595"
---
# <a name="ivmfloppydrivecollection-interface"></a>Interfaz IVMFstonepyDriveCollection

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define una colección de disquetes dentro de la máquina virtual. Para obtener un **objeto IVMFstonepyDriveCollection,** use la [**propiedad IVMVirtualMachine::FloppyDrives.**](ivmvirtualmachine-floppydrives.md)

## <a name="members"></a>Miembros

La **interfaz IVMFstonepyDriveCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFstonepyDriveCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMFstonepyDriveCollection** tiene estas propiedades.



| Propiedad                                                          | Tipo de acceso          | Descripción                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                |
| [**Contar**](ivmfloppydrivecollection-count.md)<br/>        | Solo lectura<br/> | Número de disquetes de esta colección.<br/>                  |
| [**Elemento**](ivmfloppydrivecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de unidad de disquete que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFstonepyDriveCollection se define como 8ba70a25-f698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMFstonepyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

