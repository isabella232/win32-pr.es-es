---
title: Interfaz IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Define la colección de unidades de CD y DVD de la máquina virtual. Para obtener un objeto IVMDVDDriveCollection, use la propiedad DVDROMDrives de IVMVirtualMachine.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Interfaz IVMDVDDriveCollection Virtual PC
- Interfaz IVMDVDDriveCollection Virtual PC, descripción
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
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651404"
---
# <a name="ivmdvddrivecollection-interface"></a>Interfaz IVMDVDDriveCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de unidades de CD y DVD de la máquina virtual. Para obtener un objeto **IVMDVDDriveCollection** , use la propiedad [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Miembros

La interfaz **IVMDVDDriveCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDriveCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMDVDDriveCollection** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso          | Descripción                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                   |
| [**Contabiliza**](ivmdvddrivecollection-count.md)<br/>        | Solo lectura<br/> | El número de unidades de CD y DVD de esta colección.<br/>                 |
| [**Elemento**](ivmdvddrivecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de unidad de CD o DVD que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection se define como bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine::D VDROMDrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

