---
title: Propiedad IVMTask ErrorDescription (VPCCOMInterfaces. h)
description: Recupera la descripción de error localizada registrada para esta tarea.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- Propiedad ErrorDescription Virtual PC
- Propiedad ErrorDescription Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad ErrorDescription
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803475"
---
# <a name="ivmtaskerrordescription-property"></a>IVMTask:: ErrorDescription (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la descripción de error localizada registrada para esta tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a>Valor de propiedad

Descripción de error.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El valor del parámetro es **null**.<br/>  |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

