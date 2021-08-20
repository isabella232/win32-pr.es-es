---
title: Interfaz IVMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Define la interfaz de eventos saliente para la interfaz IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- IVMVirtualMachineEvents interface Virtual PC
- IVMVirtualMachineEvents interface Virtual PC , descrito
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
ms.openlocfilehash: c6686585333f33d4732284ab448a82ac722fea03315b08aaa276f2eeabaf2e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122625"
---
# <a name="ivmvirtualmachineevents-interface"></a>IVMVirtualMachineEvents (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la interfaz de eventos saliente para [**la interfaz IVMVirtualMachine.**](ivmvirtualmachine.md) El cliente implementa estos métodos para recibir eventos enviados desde [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="members"></a>Miembros

La **interfaz IVMVirtualMachineEvents** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualMachineEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IVMVirtualMachineEvents** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Recibe la notificación de que los componentes de integración están disponibles en una máquina virtual.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Recibe la notificación de que los componentes de integración se desinstalan en una máquina virtual.<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Recibe la notificación de que ha cambiado un valor en la configuración de esta máquina virtual.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Recibe la notificación de que un disco necesario para una máquina virtual está sin espacio y la máquina virtual no se puede ejecutar.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Recibe la notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Recibe la notificación de que un usuario ha cerrado la sesión del sistema operativo invitado.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Recibe la notificación de que el sistema operativo invitado se ha apagado.<br/>                                                                     |
| [**OnBeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Recibe la notificación de que se ha detenido el latido de una máquina virtual. Esto suele indicar que el sistema operativo invitado se ha bloqueado.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Recibe la notificación de que se ha realizado una solicitud de cierre.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Recibe la notificación de que se ha restablecido una máquina virtual.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Recibe la notificación de que el estado de una máquina virtual ha cambiado.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Recibe la notificación de que una máquina virtual tiene un triple error.<br/>                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



 

