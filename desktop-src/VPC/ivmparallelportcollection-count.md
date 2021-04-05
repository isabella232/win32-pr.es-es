---
title: Propiedad de recuento de IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Número de puertos paralelos de esta colección.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMParallelPortCollection
- Interfaz IVMParallelPortCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996484"
---
# <a name="ivmparallelportcollectioncount-property"></a>IVMParallelPortCollection:: Count (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número de puertos paralelos de esta colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor de propiedad

El número de puertos paralelos.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                            | Significado                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>               | La operación se realizó correctamente.<br/> |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl> | El parámetro es **null**.<br/>    |



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

 

