---
title: Propiedad _NewEnum IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum propiedad Virtual PC
- _NewEnum propiedad Virtual PC , interfaz IVMHardDiskConnectionCollection
- IVMHardDiskConnectionCollection interface Virtual PC , _NewEnum propiedad
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection._NewEnum
- IVMHardDiskConnectionCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02c4bbd5d0d54d5116adc09c3a0a23c4594834b48b1b28d1700d41e5525b5d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510805"
---
# <a name="ivmharddiskconnectioncollection_newenum-property"></a>IVMHardDiskConnectionCollection:: \_ Propiedad NewEnum

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
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                               |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID IVMHardDiskconnectionCollection se define como \_ b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

