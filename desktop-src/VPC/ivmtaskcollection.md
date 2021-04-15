---
title: Interfaz IVMTaskCollection (VPCCOMInterfaces. h)
description: Define la colección de objetos Task. Para obtener un objeto IVMTaskCollection, use la propiedad Tasks de IVMVirtualPC.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Interfaz IVMTaskCollection Virtual PC
- Interfaz IVMTaskCollection Virtual PC, descripción
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
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422505"
---
# <a name="ivmtaskcollection-interface"></a>Interfaz IVMTaskCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de objetos Task. Para obtener un objeto **IVMTaskCollection** , use la propiedad [**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md) .

## <a name="members"></a>Miembros

La interfaz **IVMTaskCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMTaskCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMTaskCollection** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                        |
| [**Contabiliza**](ivmtaskcollection-count.md)<br/>        | Solo lectura<br/> | Número de tareas de esta colección.<br/>                  |
| [**Elemento**](ivmtaskcollection-item.md)<br/>          | Solo lectura<br/> | Objeto de tarea que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection se define como 5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

