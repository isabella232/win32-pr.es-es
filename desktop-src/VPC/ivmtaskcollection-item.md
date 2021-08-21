---
title: Propiedad IVMTaskCollection Item (VPCCOMInterfaces.h)
description: Recupera el objeto de tarea que corresponde al índice especificado.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Propiedad de elemento Virtual PC
- Propiedad de elemento Virtual PC , interfaz IVMTaskCollection
- IVMTaskCollection interface Virtual PC , Propiedad Item
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d721bcd990ab84e763003f3fff457fec41ec9dd3764797c373e2d094fa288526
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958835"
---
# <a name="ivmtaskcollectionitem-property"></a>IVMTaskCollection::Item, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el objeto de tarea que corresponde al índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMTask.**](ivmtask.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente. <br/>                                                      |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El *parámetro task* es **NULL.** <br/>                                                  |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | El índice del elemento solicitado no corresponde a un elemento de esta colección. <br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMTaskCollection se define como \_ 5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMTaskCollection**](ivmtaskcollection.md)
</dt> </dl>

 

