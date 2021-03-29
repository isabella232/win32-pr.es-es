---
title: Interfaz IVMTask (VPCCOMInterfaces. h)
description: Use la interfaz IVMTask para supervisar y controlar tareas asincrónicas para varios métodos COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Interfaz IVMTask Virtual PC
- Interfaz IVMTask Virtual PC, descripción
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
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534768"
---
# <a name="ivmtask-interface"></a>Interfaz IVMTask

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Use la interfaz **IVMTask** para supervisar y controlar tareas asincrónicas para varios métodos com.

## <a name="members"></a>Miembros

La interfaz **IVMTask** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMTask** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMTask** tiene estos métodos.



| Método                                                 | Descripción                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Cancelar**](ivmtask-cancel.md)                       | Cancela la tarea.<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMTask** tiene estas propiedades.



| Propiedad                                                        | Tipo de acceso          | Descripción                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Descripción**](ivmtask-description.md)<br/>           | Solo lectura<br/> | Una descripción de la tarea.<br/>                              |
| [**Error**](ivmtask-error.md)<br/>                       | Solo lectura<br/> | Error registrado para esta tarea.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Solo lectura<br/> | La descripción de error localizada registrada para esta tarea.<br/> |
| [**id**](ivmtask-id.md)<br/>                             | Solo lectura<br/> | Identificador único para esta tarea.<br/>                      |
| [**IsCancelable**](ivmtask-iscancelable.md)<br/>         | Solo lectura<br/> | Indica si la tarea se puede cancelar.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Solo lectura<br/> | Indica si la tarea se ha completado.<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | Solo lectura<br/> | Porcentaje de finalización de la tarea.<br/>                  |
| [**Resultado**](ivmtask-result.md)<br/>                     | Solo lectura<br/> | Resultado de la tarea.<br/>                                 |



 

## <a name="remarks"></a>Observaciones

Un objeto **IVMTask** es devuelto por métodos que podrían requerir una cantidad considerable de tiempo para completarse. Esto permite que la aplicación supervise el progreso de la operación deseada sin forzarla a bloquear la ejecución mientras se espera la finalización de la operación.

Los métodos siguientes devuelven un objeto **IVMTask** que se puede usar para realizar el seguimiento del progreso:

-   [**IVMGuestOS:: Logoff**](ivmguestos-logoff.md)
-   [**IVMGuestOS:: restart**](ivmguestos-restart.md)
-   [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk:: Compact**](ivmharddisk-compact.md)
-   [**IVMHardDisk:: Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk:: Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk:: Mergeto**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine:: RESET**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine:: startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine:: Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine:: desapagar**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



 

