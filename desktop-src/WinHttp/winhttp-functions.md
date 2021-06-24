---
description: En este tema se identifican las funciones que proporciona WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funciones WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587747"
---
# <a name="winhttp-functions"></a>Funciones WinHTTP

WinHTTP proporciona las siguientes funciones:

<dl> <dt>

[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

Agrega uno o varios encabezados de solicitud HTTP al identificador de solicitud HTTP.

</dd> <dt>

[**WinHttpCheckPlatform**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

Determina si WinHTTP admite la plataforma actual.

</dd> <dt>

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

Cierra un único identificador [HINTERNET.](hinternet-handles-in-winhttp.md)

</dd> <dt>

[**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

Especifica el servidor de destino inicial de una solicitud HTTP.

</dd> <dt>

[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

Separa una dirección URL en sus elementos componentes, por ejemplo, el nombre de host y la ruta de acceso.

</dd> <dt>

[**WinHttpCreateProxyResolver**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

Crea un identificador para que [**lo use WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)

</dd> <dt>

[**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

Crea una dirección URL a partir de elementos de componente, por ejemplo, el nombre de host y la ruta de acceso.

</dd> <dt>

[**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

Busca la dirección URL del archivo de configuración automática (PAC) del proxy. Esta función notifica la dirección URL del archivo PAC, pero no descarga el archivo.

</dd> <dt>

[**WinHttpFreeProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

Libera los datos recuperados de una llamada anterior a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)

</dd> <dt>

[**WinHttpFreeQueryConnectionGroupResult**](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

Libera la memoria asignada por una llamada anterior a [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).

</dd> <dt>

[**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

Recupera la configuración predeterminada del proxy WinHTTP del Registro.

</dd> <dt>

[**WinHTTPGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

Obtiene la configuración Internet Explorer proxy (IE) del usuario actual.

</dd> <dt>

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

Recupera la información de proxy de la dirección URL especificada.

</dd> <dt>

[**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

Recupera la información de proxy de la dirección URL especificada.

</dd> <dt>

[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

Recupera los resultados de una llamada a [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)

</dd> <dt>

[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

Inicializa el uso de las funciones WinHTTP de una aplicación.

</dd> <dt>

[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

Crea un identificador de solicitud HTTP.

</dd> <dt>

[**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

Devuelve los esquemas de autorización que admite el servidor.

</dd> <dt>

[**WinHttpQueryConnectionGroup**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

Recupera una descripción del estado actual de las conexiones de WinHttp.

</dd> <dt>

[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

Devuelve el número de bytes de datos que están disponibles inmediatamente para leerse [**con WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)

</dd> <dt>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

Recupera la información de encabezado asociada a una solicitud HTTP.

</dd> <dt>

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

Consulta una opción de Internet en el identificador especificado.

</dd> <dt>

[**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

Lee datos de un identificador abierto por la [**función WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)

</dd> <dt>

[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

Finaliza una solicitud HTTP iniciada por [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

</dd> <dt>

[**WinHttpResetAutoProxy**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

Restablece el proxy automático.

</dd> <dt>

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

Envía la solicitud especificada al servidor HTTP.

</dd> <dt>

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

Pasa las credenciales de autorización necesarias al servidor.

</dd> <dt>

[**WinHttpSetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

Establece la configuración predeterminada del proxy WinHTTP en el Registro.

</dd> <dt>

[**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

Establece una opción de Internet.

</dd> <dt>

[**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

Configura una función de devolución de llamada a la que WinHTTP puede llamar a medida que se realiza el progreso durante una operación.

</dd> <dt>

[**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

Establece los distintos tiempos de espera que implican las transacciones HTTP.

</dd> <dt>

[**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

Da formato a una fecha y hora según la especificación http versión 1.0.

</dd> <dt>

[**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

Toma una cadena de fecha y hora HTTP y la convierte en una [**estructura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

[**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

Escribe datos de solicitud en un servidor HTTP.

</dd> <dt>

[**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

Cierra una conexión de WebSocket.

</dd> <dt>

[**WinHttpWebSocketCompleteUpgrade**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

Completa un protocolo de enlace WebSocket iniciado [**por WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

</dd> <dt>

[**WinHttpWebSocketQueryCloseStatus**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

Obtiene el estado de cierre enviado por un servidor.

</dd> <dt>

[**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

Recibe datos de una conexión webSocket.

</dd> <dt>

[**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

Envía datos a través de una conexión webSocket.

</dd> <dt>

[**WinHttpWebSocketShutdown**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

Envía un fotograma cercano a una conexión de WebSocket.

</dd> </dl>

 

 
