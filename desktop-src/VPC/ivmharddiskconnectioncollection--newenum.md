---
title: Propiedad _NewEnum IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMHardDiskConnectionCollection
- Interfaz IVMHardDiskConnectionCollection Virtual PC, propiedad _NewEnum
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
ms.openlocfilehash: 66a6e8d5278b0aa164e2bc1ffd75b07a54300b45
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698045"
---
# <a name="ivmharddiskconnectioncollection_newenum-property"></a>IVMHardDiskConnectionCollection:: \_ NewEnum (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un enumerador para la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Valor de propiedad

Enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/> |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>    |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se ha producido un error inesperado.<br/> |



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

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

