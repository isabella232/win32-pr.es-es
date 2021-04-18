---
title: Enumeraciones de registro de eventos de Windows
description: El registro de eventos de Windows define las enumeraciones siguientes.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695413"
---
# <a name="windows-event-log-enumerations"></a>Enumeraciones de registro de eventos de Windows

El registro de eventos de Windows define las enumeraciones siguientes.



| Enumeración                                                                          | Descripción                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ reloj del canal de EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Define los valores que especifican el tipo de marca de tiempo que se va a usar al registrar el canal de eventos.                                         |
| [**\_ \_ \_ ID. de propiedad de configuración de canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Define los identificadores que identifican las propiedades de configuración de un canal.                                                   |
| [**\_tipo de \_ aislamiento de canal de EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Define los permisos de acceso predeterminados que se van a aplicar al canal.                                                                    |
| [**\_indicadores de \_ Referencia del canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Define los valores que especifican cómo se hace referencia a un canal.                                                                       |
| [**\_tipo de \_ SID de canal de EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Define los valores que determinan si el evento incluye el identificador de seguridad (SID) de la entidad de seguridad que registró el evento. |
| [**\_tipo de canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Define el tipo de un canal.                                                                                                     |
| [**EVT \_ \_ identificador de propiedad de metadatos de evento \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Define los identificadores que identifican las propiedades de metadatos de una definición de evento.                                              |
| [**identificador de la \_ propiedad de evento evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Define los valores que determinan la información de la consulta que se va a recuperar.                                                               |
| [**EVT \_ marcas de EXPORTLOG \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Define valores que indican si los eventos proceden de un canal o un archivo de registro.                                                   |
| [**EVT \_ formato \_ de \_ marcas de mensaje**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Define los valores que especifican la cadena de mensaje del evento al que se va a dar formato.                                                       |
| [**identificador de la \_ propiedad de registro evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Define los identificadores que identifican las propiedades de metadatos del archivo de registro de un canal o un archivo de registro.                                   |
| [**EVT ( \_ clase de inicio de sesión) \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Define los tipos de métodos de conexión que puede usar para conectarse al equipo remoto.                                             |
| [**EVT \_ abrir \_ marcas de registro \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Define los valores que especifican si se debe abrir un canal o un archivo de registro exportado.                                                    |
| [**\_identificador de \_ propiedad de metadatos del publicador de \_ evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Define los identificadores que identifican las propiedades de metadatos de un proveedor.                                                       |
| [**EVT ( \_ marcas de consulta) \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Define los valores que especifican cómo se devuelven los resultados de la consulta y si se realiza una consulta en un canal o un archivo de registro.           |
| [**identificador de la \_ propiedad de consulta evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Define los identificadores que identifican la información de consulta que puede recuperar.                                                 |
| [**EVT \_ - \_ representar \_ marcas de contexto**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Define los valores que especifican el tipo de información a la que se obtiene acceso desde el evento.                                                  |
| [**EVT- \_ representar \_ marcas**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Define los valores que especifican lo que se va a representar.                                                                                    |
| [**EVT \_ \_ marcas de inicio de sesión RPC \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Define los tipos de autenticación que puede usar para autenticar al usuario al conectarse a un equipo remoto.                |
| [**EVT \_ Buscar \_ marcas**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Define la posición relativa en el conjunto de resultados a partir del cual se va a buscar.                                                                |
| [**las \_ marcas de suscripción de EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Define los valores posibles que especifican Cuándo se debe iniciar la suscripción a eventos.                                                      |
| [**EVT \_ suscripción a la \_ acción de notificación \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Define los posibles tipos de datos que el servicio de suscripción puede enviar a la devolución de llamada.                                     |
| [**EVT \_ \_ ID. de propiedad del sistema \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Define los identificadores que identifican las propiedades definidas por el sistema de un evento.                                                   |
| [**EVT ( \_ tipo de variante) \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Define los posibles tipos de datos de un elemento de datos Variant.                                                                            |



 

 

 




