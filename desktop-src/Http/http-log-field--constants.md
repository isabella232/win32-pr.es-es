---
title: HTTP_LOG_FIELD_ constantes (Http.h)
description: Defina los campos del registro W3C y los registros de errores.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616caaed9829c7f926f95f8982033457e1835a6beccfcad8313f6624d68195db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950834"
---
# <a name="http_log_field_-constants"></a>Constantes \_ DE CAMPO DE \_ REGISTRO \_ HTTP

Las **constantes HTTP LOG \_ \_ FIELD \_** definen los campos del registro W3C y los registros de errores.

Estas constantes se usan en la estructura [**HTTP \_ LOGGING \_ INFO.**](/windows/desktop/api/Http/ns-http-http_logging_info)

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**FECHA \_ DEL CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Fecha en la que se produjo la actividad.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HORA \_ DEL CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Hora, en hora universal coordinada (UTC), a la que se produjo la actividad.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**DIRECCIÓN IP \_ DEL CLIENTE DEL CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Dirección IP del cliente que realizó la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**NOMBRE \_ DE USUARIO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nombre del usuario autenticado que ha accedido al servidor. Los usuarios anónimos se indican con un guion.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**NOMBRE \_ DEL SITIO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nombre del sitio en el que se generó la entrada del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**HTTP \_ NOMBRE DE \_ EQUIPO DEL CAMPO DE \_ \_ REGISTRO**
</dt> <dd> <dl> <dt>



Nombre del equipo en el que se generó la entrada del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**DIRECCIÓN IP \_ DEL SERVIDOR DE CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Dirección IP del servidor en el que se generó la entrada del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**MÉTODO \_ DE CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



La acción solicitada, por ejemplo, un método get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**HTTP \_ LOG \_ FIELD \_ URI \_ STEM**
</dt> <dd> <dl> <dt>



El destino de la acción, por ejemplo, Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**CONSULTA DE URI \_ DE CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Consulta, si la hay, que el cliente estaba intentando realizar. Las consultas de Identificador de recursos universal (URI) solo son necesarias para las páginas dinámicas.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**ESTADO \_ DEL CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



El código de estado HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**ESTADO \_ DE \_ WIN32 DEL CAMPO \_ DE REGISTRO \_ HTTP**
</dt> <dd> <dl> <dt>



El Windows de estado.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**BYTES \_ DE CAMPO DE REGISTRO HTTP \_ \_ \_ ENVIADOS**
</dt> <dd> <dl> <dt>



Número, en bytes, enviado por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**RECV \_ DE BYTES DE CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Número, en bytes, recibido por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**TIEMPO DE CAMPO DE REGISTRO HTTP \_ \_ \_ \_ REALIZADO**
</dt> <dd> <dl> <dt>



Tiempo, en milisegundos, de la acción.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**PUERTO \_ DEL SERVIDOR DE CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Número de puerto del servidor configurado para el servicio.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**HTTP \_ AGENTE \_ DE USUARIO DE CAMPO DE \_ \_ REGISTRO**
</dt> <dd> <dl> <dt>



Aplicación que usó el cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**COOKIE \_ DE CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Contenido de la cookie enviada o recibida, si la hay.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**REFERENCIA \_ DE CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



El sitio que el usuario visitó por última vez. Este sitio proporciona un vínculo al sitio actual.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**VERSIÓN \_ DEL CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Versión del protocolo HTTP que usó el cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HOST \_ DE CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nombre del encabezado de host, si lo hay.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_SUBESESTACIÓN \_ DE CAMPO DE \_ REGISTRO \_ HTTP**
</dt> <dd> <dl> <dt>



Código de error de subestado.


</dt> </dl> </dd> </dl>

Las siguientes constantes se usan para el registro de errores HTTP.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**PUERTO \_ DE CLIENTE DEL CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Número de puerto de cliente desde el que se recibe la solicitud. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**URI \_ DE CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Uri recibido en la solicitud, incluida la parte de la consulta. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**IDENTIFICADOR \_ DE SITIO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Identificador numérico específico de la aplicación del grupo de direcciones URL en el que se enruta la solicitud. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**MOTIVO \_ DEL CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Frase de motivo del error. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**NOMBRE DE \_ LA COLA DEL CAMPO DE REGISTRO \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nombre de la cola de solicitudes a la que se envía la solicitud. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**STREAMID \_ DE CAMPO DE REGISTRO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Id. de secuencia.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de API de servidor HTTP versión 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMACIÓN \_ DE REGISTRO \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





