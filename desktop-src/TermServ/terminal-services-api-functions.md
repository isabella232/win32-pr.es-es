---
title: Servicios de Escritorio remoto funciones de la API
description: Las siguientes funciones se usan con Servicios de Escritorio remoto.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792135"
---
# <a name="remote-desktop-services-api-functions"></a>Servicios de Escritorio remoto funciones de la API

Las siguientes funciones se usan con Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Recupera la sesión de Servicios de Escritorio remoto asociada a un proceso especificado.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Abre un identificador del servidor de licencias de Escritorio remoto especificado.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Cierra un identificador abierto a un servidor de licencias de Escritorio remoto.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Devuelve el certificado del servidor de licencias de Escritorio remoto.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Comienza la enumeración a través de todos los paquetes de claves instalados en un servidor de licencias de Escritorio remoto basado en criterios de búsqueda.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y finaliza la enumeración.

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y devuelve el siguiente paquete de claves que está instalado en un servidor de licencias escritorio remoto que coincida con los criterios de búsqueda.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Comienza la enumeración de licencias emitidas por el servidor de licencias de Escritorio remoto basado en criterios de búsqueda.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y finaliza la enumeración.

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y devuelve la siguiente licencia que se instala en un servidor de licencias escritorio remoto que coincide con los criterios de búsqueda.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Cierra el cliente final de un canal virtual.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Un punto de entrada definido por la aplicación para el archivo DLL del lado cliente de una aplicación que usa Servicios de Escritorio remoto canales virtuales.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Inicializa el acceso de un archivo DLL de cliente para Servicios de Escritorio remoto canales virtuales.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Función de devolución de llamada definida por la aplicación que Servicios de Escritorio remoto llamadas para notificar a la DLL de cliente los eventos de canal virtual.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Abre el cliente final de un canal virtual.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Función de devolución de llamada definida por la aplicación que Servicios de Escritorio remoto llamadas para notificar a la DLL del cliente los eventos de un canal virtual concreto.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Envía datos del extremo de cliente de un canal virtual a una aplicación de socio en el extremo del servidor.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Cierra un identificador abierto a un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Conecta una sesión de Servicios de Escritorio remoto a una sesión existente en el equipo local.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Crea un nuevo agente de escucha de Servicios de Escritorio remoto o configura un agente de escucha existente.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Desconecta el usuario que ha iniciado sesión de la sesión de Servicios de Escritorio remoto especificada sin cerrar la sesión.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Habilita o deshabilita las [sesiones secundarias](child-sessions.md).

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Enumera todos los agentes de escucha de Servicios de Escritorio remoto en un servidor host de sesión de escritorio remoto.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Recupera información sobre los procesos activos en un servidor host de sesión de escritorio remoto especificado.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Recupera información sobre los procesos activos en el servidor host de sesión de escritorio remoto especificado o en el servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto).

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Devuelve una lista de todos los servidores host de sesión de escritorio remoto dentro del dominio especificado.

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Recupera una lista de sesiones en un servidor host de sesión de escritorio remoto.

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Recupera una lista de sesiones en un servidor host de sesión de escritorio remoto o en un servidor host de virtualización de escritorio remoto especificados.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Libera memoria asignada por una función Servicios de Escritorio remoto.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Libera memoria que contiene las estructuras de [**información del proceso de WTS \_ \_ \_ ex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) o de la información de sesión de WTS asignada por una función servicios de escritorio remoto. [**\_ \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Recupera el identificador de sesión de la sesión de consola.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Recupera el identificador de la sesión secundaria, si está presente.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Recupera el descriptor de seguridad de un agente de escucha de Servicios de Escritorio remoto.

</dd> <dt>

[**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Determina si las sesiones secundarias están habilitadas.

</dd> <dt>

[**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Cierra una sesión de Servicios de Escritorio remoto especificada.

</dd> <dt>

[**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Abre un identificador para el servidor host de sesión de escritorio remoto especificado.

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Abre un identificador para el servidor host de sesión de escritorio remoto especificado o el servidor host de virtualización de escritorio remoto.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Recupera la información de configuración de un agente de escucha de Servicios de Escritorio remoto.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Recupera información de sesión para la sesión especificada en el servidor host de sesión de escritorio remoto especificado.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Recupera información de configuración para el usuario especificado en el controlador de dominio especificado o en el servidor host de sesión de escritorio remoto.

</dd> <dt>

[**WTSQueryUserToken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Obtiene el token de acceso principal del usuario que ha iniciado sesión especificado por el identificador de sesión.

</dd> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Registra la ventana especificada para recibir notificaciones de cambio de sesión.

</dd> <dt>

[**WTSRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Registra la ventana especificada para recibir notificaciones de cambio de sesión.

</dd> <dt>

[**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Muestra un cuadro de mensaje en el escritorio de cliente de una sesión de Servicios de Escritorio remoto especificada.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Configura el descriptor de seguridad de un agente de escucha de Servicios de Escritorio remoto.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Modifica la información de configuración del usuario especificado en el controlador de dominio especificado o en el servidor host de sesión de escritorio remoto.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Cierra (y, opcionalmente, se reinicia) el servidor host de sesión de escritorio remoto especificado.

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Inicia el control remoto de otra sesión de Servicios de Escritorio remoto. Debe llamar a esta función desde una sesión remota.

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Detiene una sesión de control remoto.

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Finaliza el proceso especificado en el servidor host de sesión de escritorio remoto especificado.

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Anula el registro de la ventana especificada para que no reciba más notificaciones de cambio de sesión.

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Anula el registro de la ventana especificada para que no reciba más notificaciones de cambio de sesión.

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Cierra un identificador de canal virtual abierto.

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Abre un identificador del extremo del servidor de un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Crea un canal virtual de forma similar a [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina todos los datos de entrada en cola enviados del cliente al servidor en un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina todos los datos de salida en cola enviados desde el servidor al cliente en un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Devuelve información sobre un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Lee los datos del extremo del servidor de un canal virtual.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Escribe datos en el extremo del servidor de un canal virtual.

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Espera un evento Servicios de Escritorio remoto antes de volver al llamador.

</dd> </dl>

 

 