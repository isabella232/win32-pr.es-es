---
title: Windows Enumeraciones del registro de eventos
description: Windows El registro de eventos define las enumeraciones siguientes.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241520"
---
# <a name="windows-event-log-enumerations"></a>Windows Enumeraciones del registro de eventos

Windows El registro de eventos define las enumeraciones siguientes.



| Enumeración                                                                          | Descripción                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE RELOJ \_ DEL CANAL \_ EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Define los valores que especifican el tipo de marca de tiempo que se usará al registrar el canal de eventos.                                         |
| [**ID. DE PROPIEDAD \_ DE CONFIGURACIÓN DEL CANAL \_ \_ \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Define los identificadores que identifican las propiedades de configuración de un canal.                                                   |
| [**TIPO DE AISLAMIENTO \_ DE \_ CANAL EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Define los permisos de acceso predeterminados que se aplicarán al canal.                                                                    |
| [**MARCAS DE REFERENCIA \_ \_ DEL CANAL EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Define los valores que especifican cómo se hace referencia a un canal.                                                                       |
| [**TIPO DE \_ \_ SID DE CANAL EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Define los valores que determinan si el evento incluye el identificador de seguridad (SID) de la entidad de seguridad que registró el evento. |
| [**TIPO DE \_ CANAL EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Define el tipo de un canal.                                                                                                     |
| [**ID. DE PROPIEDAD \_ DE METADATOS \_ DE EVENTOS \_ \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Define los identificadores que identifican las propiedades de metadatos de una definición de evento.                                              |
| [**ID. DE \_ PROPIEDAD \_ DEL EVENTO \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Define los valores que determinan la información de consulta que se debe recuperar.                                                               |
| [**MARCAS \_ DE EVT \_ EXPORTLOG**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Define valores que indican si los eventos proceden de un canal o un archivo de registro.                                                   |
| [**MARCAS DE MENSAJES \_ \_ CON FORMATO EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Define los valores que especifican la cadena de mensaje del evento al que se debe dar formato.                                                       |
| [**ID. DE PROPIEDAD \_ \_ DEL REGISTRO DE EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Define los identificadores que identifican las propiedades de metadatos del archivo de registro de un canal o archivo de registro.                                   |
| [**EVT \_ LOGIN \_ (CLASE)**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Define los tipos de métodos de conexión que puede usar para conectarse al equipo remoto.                                             |
| [**MARCAS DE REGISTRO \_ \_ \_ ABIERTAS DE EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Define los valores que especifican si se debe abrir un canal o un archivo de registro exportado.                                                    |
| [**ID. DE PROPIEDAD \_ DE \_ METADATOS \_ DEL PUBLICADOR DE \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Define los identificadores que identifican las propiedades de metadatos de un proveedor.                                                       |
| [**MARCAS DE \_ CONSULTA \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Define los valores que especifican cómo devolver los resultados de la consulta y si se consulta con un canal o un archivo de registro.           |
| [**ID. DE \_ PROPIEDAD \_ DE CONSULTA EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Define los identificadores que identifican la información de consulta que se puede recuperar.                                                 |
| [**MARCAS DE CONTEXTO \_ DE \_ REPRESENTACIÓN \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Define los valores que especifican el tipo de información a la que se tiene acceso desde el evento.                                                  |
| [**MARCAS DE REPRESENTACIÓN DE EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Define los valores que especifican lo que se va a representar.                                                                                    |
| [**MARCAS DE INICIO \_ DE SESIÓN DE RPC \_ \_ DE EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Define los tipos de autenticación que puede usar para autenticar al usuario al conectarse a un equipo remoto.                |
| [**MARCAS DE \_ EVT \_ SEEK**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Define la posición relativa en el conjunto de resultados desde el que se va a buscar.                                                                |
| [**MARCAS DE SUSCRIPCIÓN DE EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Define los valores posibles que especifican cuándo empezar a suscribirse a eventos.                                                      |
| [**ACCIÓN DE NOTIFICACIÓN \_ DE SUSCRIPCIÓN \_ DE EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Define los posibles tipos de datos que el servicio de suscripción puede entregar a la devolución de llamada.                                     |
| [**ID. DE \_ PROPIEDAD \_ DEL SISTEMA \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Define los identificadores que identifican las propiedades definidas por el sistema de un evento.                                                   |
| [**TIPO DE \_ VARIANTE EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Define los posibles tipos de datos de un elemento de datos variante.                                                                            |



 

 

 




