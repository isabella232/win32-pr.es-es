---
title: Propiedad _NewEnum IVMVirtualMachineCollection (VPCCOMInterfaces.h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMVirtualMachineCollection (VPCCOMInterfaces.h)
ms.assetid: 86b51542-139c-4e2b-baec-2c90956d99b3
keywords:
- _NewEnum propiedad Virtual PC
- _NewEnum propiedad Virtual PC , IVMVirtualMachineCollection (interfaz)
- IVMVirtualMachineCollection interface Virtual PC , _NewEnum propiedad
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection._NewEnum
- IVMVirtualMachineCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ddab3c42a59eec2a34ec679e57e5ac7da958004f8e9cd1be7f1c83dd6158193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752059"
---
# <a name="ivmvirtualmachinecollection_newenum-property"></a>IVMVirtualMachineCollection:: \_ Propiedad NewEnum

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un enumerador para la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Valor de propiedad

Enumerador [IEnumVARIANT.](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>    |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se ha producido un error inesperado.<br/> |



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

[**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

