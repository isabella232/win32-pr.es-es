---
title: Interfaz IVMParallelPort (VPCCOMInterfaces. h)
description: Define un puerto paralelo dentro de una máquina virtual.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Interfaz IVMParallelPort Virtual PC
- Interfaz IVMParallelPort Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696040"
---
# <a name="ivmparallelport-interface"></a>Interfaz IVMParallelPort

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define un puerto paralelo dentro de una máquina virtual. Esta interfaz permite configurar puertos paralelos dentro de una máquina virtual. Puede recuperar un objeto **IVMParallelPort** del objeto [**IVMParallelPortCollection**](ivmparallelportcollection.md) devuelto desde la propiedad [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Miembros

La interfaz **IVMParallelPort** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPort** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMParallelPort** tiene estos métodos.



| Método                              | Descripción                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [**\_id**](ivmparallelport--id.md) | Recupera el identificador interno del puerto paralelo.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMParallelPort** tiene estas propiedades.



| Propiedad                                        | Tipo de acceso           | Descripción                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [**Name**](ivmparallelport-name.md)<br/> | Lectura/escritura<br/> | Nombre del puerto paralelo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort se define como 097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



 

