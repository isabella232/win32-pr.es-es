---
title: Servicios de Escritorio remoto estructuras de API
description: Muestra las estructuras que se usan con Servicios de Escritorio remoto API.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149298"
---
# <a name="remote-desktop-services-api-structures"></a>Servicios de Escritorio remoto estructuras de API

Las siguientes estructuras se usan con la API de Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**DEF. de canal \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contiene el nombre y las opciones de un canal virtual Servicios de Escritorio remoto.

</dd> <dt>

[**\_puntos de entrada de canal \_**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contiene punteros a las funciones a las que llama un archivo DLL del lado cliente para tener acceso a los canales virtuales.

</dd> <dt>

[**\_encabezado de PDU de canal \_**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contiene información sobre un bloque de datos que recibe el servidor de un canal virtual.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contiene información sobre un paquete de claves de licencias de Servicios de Escritorio remoto específico.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contiene información acerca de una licencia de Servicios de Escritorio remoto específica.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contiene información sobre un cliente de Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contiene información sobre una sesión de Servicios de Escritorio remoto.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contiene información sobre una sesión de Servicios de Escritorio remoto.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contiene una Unión de [**\_ nivel WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) que contiene información extendida sobre una sesión de servicios de escritorio remoto.

</dd> <dt>

[**WTSINFOEX \_ Level1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contiene información extendida sobre una sesión de Servicios de Escritorio remoto.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contiene información sobre un agente de escucha de Servicios de Escritorio remoto.

</dd> <dt>

[**\_dirección IP de WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contiene información acerca de la dirección IP de un recurso de red.

</dd> <dt>

[**información de conexión a la \_ máquina WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contiene información acerca de un equipo que acepta conexiones remotas.

</dd> <dt>

[**información de la \_ máquina WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contiene información acerca de un equipo y su estado actual.

</dd> <dt>

[**\_información de sesión de WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Contiene información sobre las sesiones que están disponibles para el agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto).

</dd> <dt>

[**\_notificación WTSSESSION**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Proporciona información sobre la notificación de cambio de sesión. Un servicio recibe esta estructura en su función [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) en respuesta a un evento de cambio de sesión.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contiene información de configuración para un usuario en un controlador de dominio o un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).

</dd> <dt>

[**\_dirección de cliente de WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contiene la dirección de red de cliente de una sesión de Servicios de Escritorio remoto.

</dd> <dt>

[**\_pantalla de cliente de WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contiene información acerca de la presentación de un cliente de Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**\_información del proceso de WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contiene información sobre un proceso que se ejecuta en un servidor host de sesión de escritorio remoto.

</dd> <dt>

[**información del proceso de WTS \_ \_ \_ ex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contiene información extendida sobre un proceso que se ejecuta en un servidor host de sesión de escritorio remoto.

</dd> <dt>

[**\_información del producto de WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Los detalles de la licencia de producto necesarios para conectarse a un servidor de Terminal Server.

</dd> <dt>

[**\_información del servidor de WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contiene información acerca de un servidor de Servicios de Escritorio remoto específico.

</dd> <dt>

[**\_dirección de sesión de WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contiene la dirección IP virtual asignada a una sesión.

</dd> <dt>

[**\_información de sesión de WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contiene información sobre una sesión de cliente en un servidor host de sesión de escritorio remoto.

</dd> <dt>

[**Información de sesión de WTS \_ \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contiene información extendida sobre una sesión de cliente en un servidor host de sesión de escritorio remoto o en un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto).

</dd> </dl>

 

 