---
title: Propiedad IVMTask PercentCompleted (VPCCOMInterfaces.h)
description: Recupera el porcentaje de finalización de la tarea.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- PercentCompleted, propiedad Virtual PC
- Propiedad PercentCompleted Virtual PC , interfaz IVMTask
- Interfaz IVMTask Pc virtual, propiedad PercentCompleted
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb15d187b4e9246c0c7a5b0af03e0ab8a9eec2bb6b8b9242120f9faf4c6fc96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958865"
---
# <a name="ivmtaskpercentcompleted-property"></a>IVMTask::P centCompleted

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el porcentaje de finalización de la tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a>Valor de propiedad

Porcentaje de finalización actual. El valor es un número entre 0 y 100.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El valor del parámetro es **NULL.**<br/>  |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMTask se define como \_ ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

