---
title: Propiedad IVMGuestOS ProductType (VPCCOMInterfaces. h)
description: Recupera el tipo de producto del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Propiedad ProductType Virtual PC
- Propiedad ProductType Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676745"
---
# <a name="ivmguestosproducttype-property"></a>IVMGuestOS::P propiedad roductType

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el tipo de producto del sistema operativo invitado que se ejecuta en la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a>Valor de propiedad

El tipo de producto. Se admiten los siguientes valores de cadena.



| Value                                                                                  | Significado                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x0000002"</dt> </dl> | El sistema es un controlador de dominio y el sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | El sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/> Tenga en cuenta que un servidor que también es un controlador de dominio se indica como controlador de dominio de NT de ver, no como **\_ \_ servidor de NT**. **\_ \_ \_**<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | El sistema operativo es Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

