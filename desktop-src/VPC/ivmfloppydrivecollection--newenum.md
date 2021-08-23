---
title: Propiedad _NewEnum IVMFstonepyDriveCollection (VPCCOMInterfaces.h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMFstonepyDriveCollection (VPCCOMInterfaces.h)
ms.assetid: 06de9560-cba9-4c64-907e-83e77781cafc
keywords:
- _NewEnum propiedad Virtual PC
- _NewEnum propiedad Virtual PC , interfaz IVMFstonepyDriveCollection
- IVMFstonepyDriveCollection interface Virtual PC , _NewEnum propiedad
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection._NewEnum
- IVMFloppyDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceac8ef29e659269a34687f9b32c74c7f0da2d6562343c1fc8588e07230d5b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653675"
---
# <a name="ivmfloppydrivecollection_newenum-property"></a>IVMFstonepyDriveCollection:: \_ Propiedad NewEnum

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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFstonepyDriveCollection se define como 8ba70a25-f698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDriveCollection**](ivmfloppydrivecollection.md)
</dt> </dl>

 

