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
# <a name="http_log_field_-constants"></a><span data-ttu-id="f70cc-103">\_Constantes de \_ campo de registro http \_</span><span class="sxs-lookup"><span data-stu-id="f70cc-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="f70cc-104">Las constantes de **\_ \_ campo \_ de registro http** definen los campos en el registro del W3C y los registros de errores.</span><span class="sxs-lookup"><span data-stu-id="f70cc-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="f70cc-105">Estas constantes se utilizan en la estructura [**de \_ \_ información de registro http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="f70cc-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="f70cc-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_fecha del \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-107">Fecha en la que se produjo la actividad.</span><span class="sxs-lookup"><span data-stu-id="f70cc-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_hora del \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-109">La hora, en hora universal coordinada (UTC), a la que se produjo la actividad.</span><span class="sxs-lookup"><span data-stu-id="f70cc-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_ \_ \_ dirección IP del cliente del campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-111">Dirección IP del cliente que realizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f70cc-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_nombre de \_ usuario del campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-113">Nombre del usuario autenticado que tuvo acceso al servidor.</span><span class="sxs-lookup"><span data-stu-id="f70cc-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="f70cc-114">Los usuarios anónimos se indican con un guion.</span><span class="sxs-lookup"><span data-stu-id="f70cc-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_nombre del \_ sitio del campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-116">Nombre del sitio en el que se generó la entrada del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f70cc-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_nombre del \_ equipo \_ del campo de registro**</span><span class="sxs-lookup"><span data-stu-id="f70cc-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-118">Nombre del equipo en el que se generó la entrada del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f70cc-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_IP de \_ servidor de campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-120">Dirección IP del servidor en el que se generó la entrada del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f70cc-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_método de \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-122">La acción solicitada, por ejemplo, un método get.</span><span class="sxs-lookup"><span data-stu-id="f70cc-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_recurso de \_ URI \_ de campo de registro**</span><span class="sxs-lookup"><span data-stu-id="f70cc-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-124">El destino de la acción, por ejemplo, Default.htm.</span><span class="sxs-lookup"><span data-stu-id="f70cc-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_consulta de \_ URI de campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-126">La consulta, si la hay, que el cliente estaba intentando realizar.</span><span class="sxs-lookup"><span data-stu-id="f70cc-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="f70cc-127">Las consultas de Identificador de recursos universal (URI) solo son necesarias para las páginas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="f70cc-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_Estado del \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-129">El código de estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="f70cc-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_Campo de registro http \_ \_ Estado de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-131">Código de estado de Windows.</span><span class="sxs-lookup"><span data-stu-id="f70cc-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_bytes de campos de registro http \_ \_ \_ enviados**</span><span class="sxs-lookup"><span data-stu-id="f70cc-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-133">Número, en bytes, enviado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="f70cc-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_bytes de campo de registro http \_ \_ \_ recibidos**</span><span class="sxs-lookup"><span data-stu-id="f70cc-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-135">Número, en bytes, recibido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="f70cc-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**tiempo de los \_ campos de registro http \_ \_ \_ tomados**</span><span class="sxs-lookup"><span data-stu-id="f70cc-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-137">El tiempo, en milisegundos, de la acción.</span><span class="sxs-lookup"><span data-stu-id="f70cc-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_Puerto de \_ servidor de campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-139">Número de puerto del servidor que está configurado para el servicio.</span><span class="sxs-lookup"><span data-stu-id="f70cc-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ \_agente de \_ usuario \_ de campo de registro**</span><span class="sxs-lookup"><span data-stu-id="f70cc-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-141">La aplicación usada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="f70cc-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_cookie de \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-143">El contenido de la cookie enviada o recibida, si existe.</span><span class="sxs-lookup"><span data-stu-id="f70cc-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_referencia de \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-145">El sitio que el usuario visitó por última vez.</span><span class="sxs-lookup"><span data-stu-id="f70cc-145">The site that the user last visited.</span></span> <span data-ttu-id="f70cc-146">Este sitio proporciona un vínculo al sitio actual.</span><span class="sxs-lookup"><span data-stu-id="f70cc-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_versión del \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-148">La versión del protocolo HTTP que usó el cliente.</span><span class="sxs-lookup"><span data-stu-id="f70cc-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_host de \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-150">Nombre del encabezado de host, si existe.</span><span class="sxs-lookup"><span data-stu-id="f70cc-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_subestado de campo de registro http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-152">Código de error de subestado.</span><span class="sxs-lookup"><span data-stu-id="f70cc-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="f70cc-153">Las constantes siguientes se usan para el registro de errores HTTP.</span><span class="sxs-lookup"><span data-stu-id="f70cc-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="f70cc-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_Puerto de \_ cliente del campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-155">El número de puerto del cliente desde el que se recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f70cc-155">The client port number from which the request is received.</span></span> <span data-ttu-id="f70cc-156">Este campo de registro solo se usa para el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="f70cc-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI del \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-158">El URI recibido en la solicitud, incluida la parte de la consulta.</span><span class="sxs-lookup"><span data-stu-id="f70cc-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="f70cc-159">Este campo de registro solo se usa para el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="f70cc-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_identificador de \_ sitio del campo de registro http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-161">IDENTIFICADOR numérico específico de la aplicación del grupo de direcciones URL en el que se enruta la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f70cc-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="f70cc-162">Este campo de registro solo se usa para el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="f70cc-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_motivo del \_ campo de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-164">La frase del motivo del error.</span><span class="sxs-lookup"><span data-stu-id="f70cc-164">The error reason phrase.</span></span> <span data-ttu-id="f70cc-165">Este campo de registro solo se usa para el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="f70cc-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**nombre de la cola del campo de \_ registro http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-167">El nombre de la cola de solicitudes a la que se envía la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f70cc-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="f70cc-168">Este campo de registro solo se usa para el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="f70cc-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f70cc-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_campo de registro http \_ \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="f70cc-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f70cc-170">El identificador de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f70cc-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f70cc-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f70cc-171">Requirements</span></span>



| <span data-ttu-id="f70cc-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70cc-172">Requirement</span></span> | <span data-ttu-id="f70cc-173">Value</span><span class="sxs-lookup"><span data-stu-id="f70cc-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f70cc-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70cc-174">Minimum supported client</span></span><br/> | <span data-ttu-id="f70cc-175">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f70cc-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f70cc-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70cc-176">Minimum supported server</span></span><br/> | <span data-ttu-id="f70cc-177">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f70cc-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f70cc-178">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f70cc-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="f70cc-179"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="f70cc-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70cc-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="f70cc-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70cc-181">API del servidor HTTP versión 2,0 constantes</span><span class="sxs-lookup"><span data-stu-id="f70cc-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="f70cc-182">**\_información de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="f70cc-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="f70cc-183">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="f70cc-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="f70cc-184">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="f70cc-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="f70cc-185">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="f70cc-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="f70cc-186">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="f70cc-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





