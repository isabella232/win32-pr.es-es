---
description: Los servicios usan o implementan las siguientes funciones.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Funciones de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431a672e93c94e06a71812471aa3c74d0ac2f96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073554"
---
# <a name="service-functions"></a>Funciones de servicio

Los servicios usan o implementan las siguientes funciones.



| Función                                                             | Descripción                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Función de devolución de llamada definida por la aplicación que se usa [**con la función RegisterServiceCtrlHandler.**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Función de devolución de llamada definida por la aplicación que se usa [**con la función RegisterServiceCtrlHandlerEx.**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) |
| [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Registra una función para controlar las solicitudes de control de servicio.                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Registra una función para controlar las solicitudes de control de servicio extendidas.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Función definida por la aplicación que actúa como punto de partida para un servicio.                                                      |
| [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Registra un tipo de servicio con el administrador de control de servicios y el servicio Server.                                                     |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Actualiza la información de estado del administrador de control de servicios para el servicio que realiza la llamada.                                                     |
| [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Conecta el subproceso principal de un proceso de servicio al administrador de control de servicios.                                                         |



 

Los programas que controlan, configuran o interactúan con los servicios usan las siguientes funciones.



| Función                                                                 | Descripción                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Cambia los parámetros de configuración de un servicio.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Cambia los parámetros de configuración opcionales de un servicio.                                                                                 |
| [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Cierra el identificador especificado a un objeto del administrador de control de servicios o a un objeto de servicio.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Envía un código de control a un servicio.                                                                                                          |
| [**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Envía un código de control a un servicio.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Crea un objeto de servicio y lo agrega a la base de datos del administrador de control de servicios especificada.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Marca el servicio especificado para su eliminación de la base de datos del administrador de control de servicios.                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Recupera el nombre y el estado de cada servicio que depende del servicio especificado.                                                        |
| [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Enumera los servicios de la base de datos del administrador de control de servicios especificado en función del nivel de información especificado.                             |
| [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Recupera el nombre para mostrar del servicio especificado.                                                                                        |
| [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Recupera el nombre de servicio del servicio especificado.                                                                                        |
| [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Notifica el estado de arranque al administrador de control de servicios.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Permite que una aplicación reciba una notificación cuando se crea o elimina el servicio especificado o cuando cambia su estado.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Establece una conexión con el administrador de control de servicios en el equipo especificado y abre la base de datos del administrador de control de servicios especificada. |
| [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Abre un servicio existente.                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Recupera los parámetros de configuración del servicio especificado.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Recupera los parámetros de configuración opcionales del servicio especificado.                                                                   |
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Recupera información dinámica relacionada con el inicio del servicio actual.                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Recupera una copia del descriptor de seguridad asociado a un objeto de servicio.                                                               |
| [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Recupera el estado actual del servicio especificado en función del nivel de información especificado.                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Establece el descriptor de seguridad de un objeto de servicio.                                                                                           |
| [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Inicia un servicio.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Las siguientes funciones están obsoletas.<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**UnlockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
