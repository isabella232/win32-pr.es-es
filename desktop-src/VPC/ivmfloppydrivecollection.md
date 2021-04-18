---
title: Interfaz IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Define una colección de unidades de disquete en la máquina virtual.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Interfaz IVMFloppyDriveCollection Virtual PC
- Interfaz IVMFloppyDriveCollection Virtual PC, descripción
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
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422603"
---
# <a name="ivmfloppydrivecollection-interface"></a>Interfaz IVMFloppyDriveCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define una colección de unidades de disquete en la máquina virtual. Para obtener un objeto **IVMFloppyDriveCollection** , use la propiedad [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Miembros

La interfaz **IVMFloppyDriveCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMFloppyDriveCollection** tiene estas propiedades.



| Propiedad                                                          | Tipo de acceso          | Descripción                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                |
| [**Contabiliza**](ivmfloppydrivecollection-count.md)<br/>        | Solo lectura<br/> | El número de unidades de disquete de esta colección.<br/>                  |
| [**Elemento**](ivmfloppydrivecollection-item.md)<br/>          | Solo lectura<br/> | Objeto de unidad de disquete que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection se define como 8ba70a25-F698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

