---
title: Interfaz IVMTaskCollection (VPCCOMInterfaces.h)
description: Define la colección de objetos de tarea. Para obtener un objeto IVMTaskCollection, use la propiedad IVMVirtualPC Tasks.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- IVMTaskCollection interface Virtual PC
- IVMTaskCollection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150f5079258e551360f574cfd9fa0a8895d3673f5d6b38ea6a5e1c866cfbf1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958805"
---
# <a name="ivmtaskcollection-interface"></a>IVMTaskCollection (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la colección de objetos de tarea. Para obtener un **objeto IVMTaskCollection,** use la [**propiedad IVMVirtualPC::Tasks.**](ivmvirtualpc-tasks.md)

## <a name="members"></a>Miembros

La **interfaz IVMTaskCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMTaskCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMTaskCollection** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                        |
| [**Contar**](ivmtaskcollection-count.md)<br/>        | Solo lectura<br/> | Número de tareas de esta colección.<br/>                  |
| [**Elemento**](ivmtaskcollection-item.md)<br/>          | Solo lectura<br/> | Objeto de tarea que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

