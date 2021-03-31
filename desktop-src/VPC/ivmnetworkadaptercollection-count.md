---
title: Propiedad de recuento de IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Recupera el número de interfaces de red de esta colección.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMNetworkAdapterCollection
- Interfaz IVMNetworkAdapterCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149856"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a>IVMNetworkAdapterCollection:: Count (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número de interfaces de red de esta colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor de propiedad

El número de interfaces de red.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>        |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection se define como ebaeafe9-eBCD-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

