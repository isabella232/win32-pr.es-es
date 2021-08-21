---
title: Propiedad IVMVirtualPC Tasks (VPCCOMInterfaces.h)
description: Recupera una colección de tareas.
ms.assetid: bba9c4b4-c933-43c8-9fbc-f2beb59867cf
keywords:
- Propiedad Tareas Pc virtual
- Propiedad Tareas Pc virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , propiedad Tasks
topic_type:
- apiref
api_name:
- IVMVirtualPC.Tasks
- IVMVirtualPC.get_Tasks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03e0992ff177f33c1f47ac78d0ffec94d59c330b810a796aa78530b9092b71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056543"
---
# <a name="ivmvirtualpctasks-property"></a>IVMVirtualPC::Tasks, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una colección de tareas.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Tasks(
  [out, retval] IVMTaskCollection **taskCollection
);
```



## <a name="property-value"></a>Valor de propiedad

Colección de objetos [**IVMTask.**](ivmtask.md) Vea [**IVMTaskCollection.**](ivmtaskcollection.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                | El parámetro es **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

