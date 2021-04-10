---
title: Propiedad _NewEnum IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMParallelPortCollection (VPCCOMInterfaces. h)
ms.assetid: 2e26fba7-bcc0-4bb3-bf89-3c62cbd2b37e
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMParallelPortCollection
- Interfaz IVMParallelPortCollection Virtual PC, propiedad _NewEnum
topic_type:
- apiref
api_name:
- IVMParallelPortCollection._NewEnum
- IVMParallelPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7b0a7330e38abaa604c84c2b703bd5d908619a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003498"
---
# <a name="ivmparallelportcollection_newenum-property"></a>IVMParallelPortCollection:: \_ NewEnum (propiedad)

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
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

