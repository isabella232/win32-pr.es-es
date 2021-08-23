---
title: Interfaz IVMDVDDriveCollection (VPCCOMInterfaces.h)
description: Define la colección de unidades de CD y DVD dentro de la máquina virtual. Para obtener un objeto IVMDVDDriveCollection, use la propiedad IVMVirtualMachine DVDROMDrives.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- IVMDVDDriveCollection interface Virtual PC
- IVMDVDDriveCollection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77225134a88ff2c66be3f53f5d3d44c9f8353d8f44077fb0862f0c943c5aec3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056863"
---
# <a name="ivmdvddrivecollection-interface"></a>Interfaz IVMDVDDriveCollection

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la colección de unidades de CD y DVD dentro de la máquina virtual. Para obtener un **objeto IVMDVDDriveCollection,** use la propiedad [**IVMVirtualMachine::D VDROMDrives.**](ivmvirtualmachine-dvdromdrives.md)

## <a name="members"></a>Miembros

La **interfaz IVMDVDDriveCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMDVDDriveCollection** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso          | Descripción                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                   |
| [**Contar**](ivmdvddrivecollection-count.md)<br/>        | Solo lectura<br/> | Número de unidades de CD y DVD de esta colección.<br/>                 |
| [**Elemento**](ivmdvddrivecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de unidad de CD o DVD que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDriveCollection se define como \_ bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine::D VDROMDrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

