---
description: Windows 7 y Windows Server 2008 R2 incluyen los siguientes elementos de programación nuevos y actualizados para los servicios.
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: Novedades de servicios para Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bd2e8bfa5426447e24485ed026f27e90fdcaa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669719"
---
# <a name="whats-new-in-services-for-windows-7"></a>Novedades de servicios para Windows 7

Windows 7 y Windows Server 2008 R2 incluyen los siguientes elementos de programación nuevos y actualizados para los servicios.

## <a name="new-capabilities"></a>Nuevas funcionalidades

Un servicio se puede registrar para iniciarse o detenerse cuando se produce un evento de desencadenador. Esto elimina la necesidad de que los servicios se inicien cuando se inicia el sistema, o para que los servicios sondeen o esperen activamente un evento; un servicio puede iniciarse cuando sea necesario, en lugar de iniciarse automáticamente tanto si hay trabajo que hacer como si no. Para obtener más información, vea [eventos de desencadenador de servicio](service-trigger-events.md).

## <a name="updated-functions"></a>Funciones actualizadas



| Función                                                        | Descripción                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | Cambia los parámetros de configuración de un servicio. Esta función admite cuentas de servicio administradas y cuentas virtuales. Para obtener más información, consulte la [Guía paso a paso de las cuentas de servicio](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | Cambia los parámetros de configuración opcionales de un servicio. Esta función admite nuevos niveles de información de configuración para los grupos de procesadores y los eventos de desencadenador de servicio.<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | Crea un objeto de servicio y lo agrega a la base de datos del administrador de control de servicios especificada. Esta función admite cuentas de servicio administradas y cuentas virtuales. Para obtener más información, consulte la [Guía paso a paso de las cuentas de servicio](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/> |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | Función de devolución de llamada definida por la aplicación que se usa con la función [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . Esta función de devolución de llamada admite códigos de control extendido nuevos para los cambios de tiempo del sistema y los eventos de desencadenador de servicio.<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | Recupera los parámetros de configuración opcionales de un servicio. Esta función admite nuevos niveles de información de configuración para los grupos de procesadores y los eventos de desencadenador de servicio.<br/>                                                                                                      |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | Actualiza la información de estado del administrador de control de servicios para el servicio que realiza la llamada. Esta función admite nuevos códigos de control extendido para los cambios de tiempo del sistema y los eventos de desencadenador de servicio.<br/>                                                                                         |



 

## <a name="new-structures"></a>Nuevas estructuras



| Estructura                                                                                       | Descripción                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**\_información de TIMECHANGE de servicio \_**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | Contiene la configuración de cambio de hora del sistema. <br/>                      |
| [**\_desencadenador de servicio**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | Representa un evento de desencadenador de servicio.<br/>                         |
| [**\_información de desencadenador de servicio \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | Contiene información de eventos de desencadenador para un servicio.<br/>           |
| [**\_elemento de \_ \_ datos específico de DESENCADENAdor de servicio \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Contiene datos específicos del desencadenador para un evento de desencadenador de servicio.<br/> |



 

 

