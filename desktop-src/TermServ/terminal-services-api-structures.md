---
title: Servicios de Escritorio remoto de API
description: Enumera las estructuras que se usan con Servicios de Escritorio remoto API.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000105"
---
# <a name="remote-desktop-services-api-structures"></a>Servicios de Escritorio remoto de API

Las siguientes estructuras se usan con Servicios de Escritorio remoto API.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contiene el nombre y las opciones de un Servicios de Escritorio remoto canal virtual.

</dd> <dt>

[**PUNTOS DE \_ ENTRADA DEL \_ CANAL**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contiene punteros a las funciones a las que llama un archivo DLL del lado cliente para acceder a los canales virtuales.

</dd> <dt>

[**ENCABEZADO \_ PDU DEL \_ CANAL**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contiene información sobre un bloque de datos que recibe el final del servidor de un canal virtual.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contiene información sobre un paquete de Servicios de Escritorio remoto de licencias específico.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contiene información sobre una licencia de Servicios de Escritorio remoto específica.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contiene información sobre un cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contiene información sobre una Servicios de Escritorio remoto sesión.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contiene información sobre una Servicios de Escritorio remoto sesión.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contiene una [**unión WTSINFOEX \_ LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) que contiene información extendida sobre una Servicios de Escritorio remoto sesión.

</dd> <dt>

[**WTSINFOEX \_ LEVEL1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contiene información extendida sobre una Servicios de Escritorio remoto sesión.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contiene información sobre un agente de Servicios de Escritorio remoto agente de escucha.

</dd> <dt>

[**DIRECCIÓN IP DE WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contiene información sobre la dirección IP de un recurso de red.

</dd> <dt>

[**INFORMACIÓN DE CONEXIÓN DE \_ LA MÁQUINA WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contiene información sobre un equipo que acepta conexiones remotas.

</dd> <dt>

[**INFORMACIÓN DE LA MÁQUINA WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contiene información sobre un equipo y su estado actual.

</dd> <dt>

[**INFORMACIÓN DE SESIÓN DE WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Contiene información sobre las sesiones que están disponibles para Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

</dd> <dt>

[**NOTIFICACIÓN \_ WTSSESSION**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Proporciona información sobre la notificación de cambio de sesión. Un servicio recibe esta estructura en su [*función HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) en respuesta a un evento de cambio de sesión.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contiene información de configuración para un usuario en un controlador de dominio o Escritorio remoto de host de sesión (host de sesión de Escritorio remoto).

</dd> <dt>

[**\_WTS DIRECCIÓN \_ DE CLIENTE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contiene la dirección de red del cliente de una Servicios de Escritorio remoto sesión.

</dd> <dt>

[**\_WTS PRESENTACIÓN \_ DEL CLIENTE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contiene información sobre la presentación de un cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**\_WTS INFORMACIÓN DEL \_ PROCESO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contiene información sobre un proceso que se ejecuta en un servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**\_WTS PROCESS \_ INFO \_ EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contiene información ampliada sobre un proceso que se ejecuta en un servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**\_WTS INFORMACIÓN DEL \_ PRODUCTO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Detalles de la licencia de producto necesaria para conectarse a un servidor terminal.

</dd> <dt>

[**\_WTS SERVER \_ INFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contiene información sobre un servidor Servicios de Escritorio remoto específico.

</dd> <dt>

[**\_WTS DIRECCIÓN DE \_ SESIÓN**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contiene la dirección IP virtual asignada a una sesión.

</dd> <dt>

[**\_WTS INFORMACIÓN DE \_ SESIÓN**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contiene información sobre una sesión de cliente en un servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**\_WTS INFORMACIÓN \_ DE SESIÓN \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contiene información ampliada sobre una sesión de cliente en un servidor host de sesión de Escritorio remoto o Escritorio remoto virtualización de host (Host de virtualización de Escritorio remoto).

</dd> </dl>

 

 