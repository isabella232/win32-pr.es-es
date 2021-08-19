---
title: Servicios de Escritorio remoto API Functions
description: Las siguientes funciones se usan con Servicios de Escritorio remoto.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434f009d15bccc1db8279e576b71f079c8d73119a2d82bb8fd313dcc1837c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000255"
---
# <a name="remote-desktop-services-api-functions"></a>Servicios de Escritorio remoto API Functions

Las siguientes funciones se usan con Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Recupera la Servicios de Escritorio remoto asociada a un proceso especificado.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Abre un identificador para el servidor de licencias Escritorio remoto especificado.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Cierra un identificador abierto a un Escritorio remoto de licencias.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Devuelve el certificado del Escritorio remoto de licencias.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Comienza la enumeración a través de todos los paquetes de claves instalados en Escritorio remoto servidor de licencias basado en criterios de búsqueda.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Continúa desde una llamada anterior a la [**función TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y finaliza la enumeración .

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y devuelve el siguiente paquete de claves instalado en un servidor de licencias de Escritorio remoto que coincida con los criterios de búsqueda.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Comienza la enumeración de licencias emitidas por el Escritorio remoto de licencias en función de los criterios de búsqueda.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Continúa desde una llamada anterior a la [**función TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y finaliza la enumeración .

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y devuelve la siguiente licencia instalada en un servidor de licencias de Escritorio remoto que coincida con los criterios de búsqueda.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Cierra el final del cliente de un canal virtual.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Punto de entrada definido por la aplicación para el archivo DLL del lado cliente de una aplicación que usa Servicios de Escritorio remoto canales virtuales.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Inicializa el acceso de un archivo DLL de cliente a Servicios de Escritorio remoto canales virtuales.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Una función de devolución de llamada definida por la aplicación que Servicios de Escritorio remoto para notificar al archivo DLL de cliente los eventos del canal virtual.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Abre el final de cliente de un canal virtual.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Función de devolución de llamada definida por la aplicación que Servicios de Escritorio remoto para notificar al archivo DLL de cliente los eventos de un canal virtual específico.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Envía datos desde el final del cliente de un canal virtual a una aplicación asociada en el extremo del servidor.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Cierra un identificador abierto a un servidor Escritorio remoto host de sesión (host de sesión de Escritorio remoto).

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Conecta una sesión Servicios de Escritorio remoto a una sesión existente en el equipo local.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Crea un nuevo agente Servicios de Escritorio remoto agente de escucha o configura un agente de escucha existente.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Desconecta el usuario que inició sesión de la sesión Servicios de Escritorio remoto sesión especificada sin cerrar la sesión.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Habilita o deshabilita sesiones [secundarias.](child-sessions.md)

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Enumera todos los agentes de Servicios de Escritorio remoto en un servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Recupera información sobre los procesos activos en un servidor host de sesión de Escritorio remoto especificado.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Recupera información sobre los procesos activos en el servidor host de sesión de Escritorio remoto especificado o Escritorio remoto Virtualización de host (Host de virtualización de Escritorio remoto) especificado.

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Devuelve una lista de todos los servidores host de sesión de Escritorio remoto dentro del dominio especificado.

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Recupera una lista de sesiones en un servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Recupera una lista de sesiones en un servidor host de sesión de Escritorio remoto especificado o en un servidor host de virtualización de Escritorio remoto.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Libera la memoria asignada por una Servicios de Escritorio remoto función.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Libera la memoria que contiene WTS [**\_ PROCESS INFO \_ \_ EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) o [**WTS SESSION INFO \_ \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) asignadas por una Servicios de Escritorio remoto función.

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Recupera el identificador de sesión de la sesión de consola.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Recupera el identificador de sesión secundario, si está presente.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Recupera el descriptor de seguridad de un agente Servicios de Escritorio remoto agente de escucha.

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

Abre un identificador para el servidor host de sesión de Escritorio remoto especificado.

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Abre un identificador para el servidor host de sesión de Escritorio remoto especificado o el servidor host de virtualización de Escritorio remoto.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Recupera la información de configuración de un agente de Servicios de Escritorio remoto cliente de escucha.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Recupera la información de sesión de la sesión especificada en el servidor host de sesión de Escritorio remoto especificado.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Recupera la información de configuración del usuario especificado en el controlador de dominio especificado o en el servidor host de sesión de Escritorio remoto.

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

Muestra un cuadro de mensaje en el escritorio del cliente de una sesión Servicios de Escritorio remoto especificada.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Configura el descriptor de seguridad de un agente de Servicios de Escritorio remoto cliente de escucha.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Modifica la información de configuración del usuario especificado en el controlador de dominio especificado o en el servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Apaga (y, opcionalmente, reinicia) el servidor host de sesión de Escritorio remoto especificado.

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Inicia el control remoto de otra Servicios de Escritorio remoto sesión. Debe llamar a esta función desde una sesión remota.

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Detiene una sesión de control remoto.

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Finaliza el proceso especificado en el servidor host de sesión de Escritorio remoto especificado.

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

Abre un identificador al final del servidor de un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Crea un canal virtual de una manera similar a [**WTSVirtualChannelOpen.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina todos los datos de entrada en cola enviados desde el cliente al servidor en un canal virtual especificado.

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

Lee datos del final del servidor de un canal virtual.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Escribe datos en el final del servidor de un canal virtual.

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Espera un evento Servicios de Escritorio remoto antes de volver al autor de la llamada.

</dd> </dl>

 

 