---
title: Constantes de HTTP_LOG_FIELD_ (http. h)
description: Defina los campos en el registro del W3C y los registros de errores.
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
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665960"
---
# <a name="http_log_field_-constants"></a>\_Constantes de \_ campo de registro http \_

Las constantes de **\_ \_ campo \_ de registro http** definen los campos en el registro del W3C y los registros de errores.

Estas constantes se utilizan en la estructura [**de \_ \_ información de registro http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_fecha del \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



Fecha en la que se produjo la actividad.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_hora del \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



La hora, en hora universal coordinada (UTC), a la que se produjo la actividad.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_ \_ \_ dirección IP del cliente del campo de registro http \_**
</dt> <dd> <dl> <dt>



Dirección IP del cliente que realizó la solicitud.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_nombre de \_ usuario del campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



Nombre del usuario autenticado que tuvo acceso al servidor. Los usuarios anónimos se indican con un guion.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_nombre del \_ sitio del campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



Nombre del sitio en el que se generó la entrada del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_nombre del \_ equipo \_ del campo de registro**
</dt> <dd> <dl> <dt>



Nombre del equipo en el que se generó la entrada del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_IP de \_ servidor de campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



Dirección IP del servidor en el que se generó la entrada del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_método de \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



La acción solicitada, por ejemplo, un método get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_recurso de \_ URI \_ de campo de registro**
</dt> <dd> <dl> <dt>



El destino de la acción, por ejemplo, Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_consulta de \_ URI de campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



La consulta, si la hay, que el cliente estaba intentando realizar. Las consultas de Identificador de recursos universal (URI) solo son necesarias para las páginas dinámicas.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_Estado del \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



El código de estado HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_Campo de registro http \_ \_ Estado de Win32 \_**
</dt> <dd> <dl> <dt>



Código de estado de Windows.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_bytes de campos de registro http \_ \_ \_ enviados**
</dt> <dd> <dl> <dt>



Número, en bytes, enviado por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_bytes de campo de registro http \_ \_ \_ recibidos**
</dt> <dd> <dl> <dt>



Número, en bytes, recibido por el servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**tiempo de los \_ campos de registro http \_ \_ \_ tomados**
</dt> <dd> <dl> <dt>



El tiempo, en milisegundos, de la acción.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_Puerto de \_ servidor de campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



Número de puerto del servidor que está configurado para el servicio.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ \_agente de \_ usuario \_ de campo de registro**
</dt> <dd> <dl> <dt>



La aplicación usada por el cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_cookie de \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



El contenido de la cookie enviada o recibida, si existe.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_referencia de \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



El sitio que el usuario visitó por última vez. Este sitio proporciona un vínculo al sitio actual.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_versión del \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



La versión del protocolo HTTP que usó el cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_host de \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



Nombre del encabezado de host, si existe.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_subestado de campo de registro http \_ \_ \_**
</dt> <dd> <dl> <dt>



Código de error de subestado.


</dt> </dl> </dd> </dl>

Las constantes siguientes se usan para el registro de errores HTTP.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_Puerto de \_ cliente del campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



El número de puerto del cliente desde el que se recibe la solicitud. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI del \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



El URI recibido en la solicitud, incluida la parte de la consulta. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_identificador de \_ sitio del campo de registro http \_ \_**
</dt> <dd> <dl> <dt>



IDENTIFICADOR numérico específico de la aplicación del grupo de direcciones URL en el que se enruta la solicitud. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_motivo del \_ campo de registro http \_**
</dt> <dd> <dl> <dt>



La frase del motivo del error. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**nombre de la cola del campo de \_ registro http \_ \_ \_**
</dt> <dd> <dl> <dt>



El nombre de la cola de solicitudes a la que se envía la solicitud. Este campo de registro solo se usa para el registro de errores.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_campo de registro http \_ \_ STREAMID**
</dt> <dd> <dl> <dt>



El identificador de la secuencia.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API del servidor HTTP versión 2,0 constantes](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_información de registro http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





