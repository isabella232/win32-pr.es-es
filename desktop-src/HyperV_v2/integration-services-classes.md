---
description: Los servicios de integración son servicios de software que se ejecutan sobre el sistema operativo invitado dentro de una máquina virtual secundaria y como parte de la pila de virtualización del sistema operativo de administración para proporcionar algún nivel de integración con el sistema operativo de administración.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Clases de Integration Services
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4d833263298b88872cbf6eda71b953798897f3ff820d0ae831b818b9c92eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694405"
---
# <a name="integration-services-classes"></a>Clases de Integration Services

Los servicios de integración son servicios de software que se ejecutan sobre el sistema operativo invitado dentro de una máquina virtual secundaria y como parte de la pila de virtualización del sistema operativo de administración para proporcionar algún nivel de integración con el sistema operativo de administración. Se usan para solucionar problemas que surgen del alto nivel de aislamiento que proporcionan las máquinas virtuales.

A continuación se ofrecen clases WMI de virtualización relacionadas con los servicios de integración.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                | Descripción                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | Representa un trabajo de operación del servicio de archivos invitado. <br/>                                                                                                                                                                                                            |
| [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Representa los parámetros para copiar un archivo del host en el invitado. <br/>                                                                                                                                                                                |
| [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**Msvm \_ GuestFileService**](msvm-guestfileservice.md) contiene un método que se puede usar para copiar un archivo en una máquina virtual desde el host de Hyper-V. <br/>                                                                                                     |
| [**Msvm \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**Msvm \_ GuestService**](msvm-guestservice.md) es la clase base abstracta para los servicios del invitado a los que se puede acceder desde el host. <br/>                                                                                                                  |
| [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Representa el estado del componente de interfaz de servicio invitado, que proporciona un mecanismo para interactuar con la máquina virtual desde las interfaces de administración del sistema host. <br/>                                                                         |
| [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Representa el estado configurado del componente de interfaz de servicio invitado. <br/>                                                                                                                                                                                 |
| [**Msvm \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Representa el estado del servicio de intercambio de pares clave-valor, que proporciona un mecanismo para intercambiar datos entre la máquina virtual y el sistema operativo que se ejecuta en el sistema operativo de administración.<br/>                                                  |
| [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Representa el estado configurado del servicio de intercambio de pares clave-valor.<br/>                                                                                                                                                                                    |
| [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | Representa un par clave-valor.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | Representa una asociación entre una instancia de [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) y una instancia de [**Msvm \_ GuestService**](msvm-guestservice.md), que representa un servicio que se ejecuta en el invitado. <br/> |
| [**ShutdownComponent de Msvm \_**](msvm-shutdowncomponent.md)<br/>                                                 | Representa el estado del servicio de apagado, que proporciona un mecanismo para apagar el sistema operativo de la máquina virtual desde las interfaces de administración del sistema host.<br/>                                                                       |
| [**Msvm \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Representa el estado configurado del servicio de apagado.<br/>                                                                                                                                                                                                   |
| [**Msvm \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | Representa el estado del servicio de sincronización de hora, que es responsable de sincronizar la hora del sistema de una máquina virtual con la hora del sistema operativo que se ejecuta en el sistema operativo de administración.<br/>                             |
| [**Msvm \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | Representa el estado configurado del servicio de sincronización de hora.<br/>                                                                                                                                                                                       |
| [**VssComponent de Msvm \_**](msvm-vsscomponent.md)<br/>                                                           | Representa el estado del servicio Servicio de instantáneas de volumen (VSS), que implementa el solicitante de VSS en el sistema operativo invitado.<br/>                                                                                                                    |
| [**VssComponentSettingData de Msvm \_**](msvm-vsscomponentsettingdata.md)<br/>                                     | Representa el estado configurado del servicio Servicio de instantáneas de volumen (VSS).<br/>                                                                                                                                                                           |



 

 

 




