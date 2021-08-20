---
title: Interfaz IVMTask (VPCCOMInterfaces.h)
description: Use la interfaz IVMTask para supervisar y controlar las tareas asincrónicas de varios métodos COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- IVMTask interface Virtual PC
- IVMTask interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e7afa39e8e95ac2a961212b3a3fe7b74e73bc8b1100ac44b34d09700ab58bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998725"
---
# <a name="ivmtask-interface"></a>Interfaz IVMTask

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Use la **interfaz IVMTask para** supervisar y controlar las tareas asincrónicas de varios métodos COM.

## <a name="members"></a>Miembros

La **interfaz IVMTask** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMTask también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMTask** tiene estos métodos.



| Método                                                 | Descripción                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Cancelar**](ivmtask-cancel.md)                       | Cancela la tarea.<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMTask** tiene estas propiedades.



| Propiedad                                                        | Tipo de acceso          | Descripción                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Descripción**](ivmtask-description.md)<br/>           | Solo lectura<br/> | Descripción de la tarea.<br/>                              |
| [**Error**](ivmtask-error.md)<br/>                       | Solo lectura<br/> | Error registrado para esta tarea.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Solo lectura<br/> | Descripción del error localizado registrada para esta tarea.<br/> |
| [**ID**](ivmtask-id.md)<br/>                             | Solo lectura<br/> | Identificador único de esta tarea.<br/>                      |
| [**IsCancelable**](ivmtask-iscancelable.md)<br/>         | Solo lectura<br/> | Indica si la tarea se puede cancelar.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Solo lectura<br/> | Indica si la tarea se ha completado.<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | Solo lectura<br/> | Porcentaje de finalización de la tarea.<br/>                  |
| [**Resultado**](ivmtask-result.md)<br/>                     | Solo lectura<br/> | Resultado de la tarea.<br/>                                 |



 

## <a name="remarks"></a>Comentarios

Los **métodos devuelven** un objeto IVMTask que podría requerir una cantidad significativa de tiempo para completarse. Esto permite a la aplicación supervisar el progreso de la operación deseada sin forzarla a bloquear la ejecución adicional mientras espera la finalización de la operación.

Los métodos siguientes devuelven un **objeto IVMTask** que se puede usar para realizar un seguimiento del progreso:

-   [**IVMGuestOS::Logoff**](ivmguestos-logoff.md)
-   [**IVMGuestOS::Restart**](ivmguestos-restart.md)
-   [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk::Compact**](ivmharddisk-compact.md)
-   [**IVMHardDisk::Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk::Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk::MergeTo**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine::Reset**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine::Startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine::Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMTask se define como \_ ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



 

