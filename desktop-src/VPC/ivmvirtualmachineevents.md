---
title: Interfaz IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Define la interfaz de eventos salientes para la interfaz IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Interfaz IVMVirtualMachineEvents Virtual PC
- Interfaz IVMVirtualMachineEvents Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492562"
---
# <a name="ivmvirtualmachineevents-interface"></a>Interfaz IVMVirtualMachineEvents

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la interfaz de eventos salientes para la interfaz [**IVMVirtualMachine**](ivmvirtualmachine.md) . El cliente implementa estos métodos para recibir los eventos enviados desde [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="members"></a>Miembros

La interfaz **IVMVirtualMachineEvents** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IVMVirtualMachineEvents** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Recibe una notificación de que los componentes de integración están disponibles en una máquina virtual.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Recibe la notificación de que los componentes de integración se desinstalan en una máquina virtual.<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Recibe la notificación de que ha cambiado un valor de la configuración de esta máquina virtual.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Recibe la notificación de que un disco necesario para una máquina virtual está sin espacio y la máquina virtual no se puede ejecutar.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Recibe una notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Recibe la notificación de que un usuario ha cerrado la sesión del sistema operativo invitado.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Recibe la notificación de que el sistema operativo invitado se ha cerrado.<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Recibe la notificación de que el latido de una máquina virtual se ha detenido. Esto normalmente indica que el sistema operativo invitado se ha bloqueado.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Recibe la notificación de que se ha realizado una solicitud de cierre.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Recibe la notificación de que una máquina virtual se ha restablecido.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Recibe la notificación de que el estado de una máquina virtual ha cambiado.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Recibe la notificación de que una máquina virtual tiene un error triple.<br/>                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



 

