---
description: Los servicios de integración son servicios de software que se ejecutan en la parte superior del sistema operativo invitado dentro de una máquina virtual secundaria y como parte de la pila de virtualización en el sistema operativo de administración para proporcionar cierto nivel de integración con el sistema operativo de administración.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Clases de Integration Services
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d60a913159c49387848b5e18a3e37b942f3e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544294"
---
# <a name="integration-services-classes"></a>Clases de Integration Services

Los servicios de integración son servicios de software que se ejecutan en la parte superior del sistema operativo invitado dentro de una máquina virtual secundaria y como parte de la pila de virtualización en el sistema operativo de administración para proporcionar cierto nivel de integración con el sistema operativo de administración. Se usan para resolver los problemas que surgen del alto nivel de aislamiento que proporcionan las máquinas virtuales.

A continuación se enumeran las clases WMI de virtualización relacionadas con Integration Services.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                | Descripción                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | Representa un trabajo de operación del servicio de archivos invitados. <br/>                                                                                                                                                                                                            |
| [**MSVM \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Representa los parámetros para copiar un archivo del host en el invitado. <br/>                                                                                                                                                                                |
| [**MSVM \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**MSVM \_ GuestFileService**](msvm-guestfileservice.md) contiene un método que se puede usar para copiar un archivo en una máquina virtual desde el host de Hyper-V. <br/>                                                                                                     |
| [**MSVM \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**MSVM \_ GuestService**](msvm-guestservice.md) es la clase base abstracta para los servicios del invitado a los que se puede tener acceso desde el host. <br/>                                                                                                                  |
| [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Representa el estado del componente de la interfaz de servicio invitado, que proporciona un mecanismo para interactuar con la máquina virtual desde las interfaces de administración en el sistema host. <br/>                                                                         |
| [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Representa el estado configurado del componente de la interfaz de servicio de invitado. <br/>                                                                                                                                                                                 |
| [**MSVM \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Representa el estado del servicio de intercambio de pares clave-valor, que proporciona un mecanismo para intercambiar datos entre la máquina virtual y el sistema operativo que se ejecuta en el sistema operativo de administración.<br/>                                                  |
| [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Representa el estado configurado del servicio de intercambio de pares clave-valor.<br/>                                                                                                                                                                                    |
| [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | Representa un par clave-valor.<br/>                                                                                                                                                                                                                               |
| [**MSVM \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | Representa una asociación entre una instancia de [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) y una instancia de [**MSVM \_ GuestService**](msvm-guestservice.md), que representa un servicio que se ejecuta en el invitado. <br/> |
| [**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md)<br/>                                                 | Representa el estado del servicio de cierre, que proporciona un mecanismo para apagar el sistema operativo de la máquina virtual desde las interfaces de administración en el sistema host.<br/>                                                                       |
| [**MSVM \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Representa el estado configurado del servicio de cierre.<br/>                                                                                                                                                                                                   |
| [**MSVM \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | Representa el estado del servicio de sincronización de hora, que es responsable de sincronizar la hora del sistema de una máquina virtual con la hora del sistema del sistema operativo que se ejecuta en el sistema operativo de administración.<br/>                             |
| [**MSVM \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | Representa el estado configurado del servicio de sincronización de hora.<br/>                                                                                                                                                                                       |
| [**MSVM \_ VssComponent**](msvm-vsscomponent.md)<br/>                                                           | Representa el estado del servicio Servicio de instantáneas de volumen (VSS), que implementa el solicitante de VSS en el sistema operativo invitado.<br/>                                                                                                                    |
| [**MSVM \_ VssComponentSettingData**](msvm-vsscomponentsettingdata.md)<br/>                                     | Representa el estado configurado del servicio Servicio de instantáneas de volumen (VSS).<br/>                                                                                                                                                                           |



 

 

 




