---
title: Confirmación para Create-Session
description: Use la confirmación de Create-Session paquete para confirmar la solicitud de Create-Session del cliente.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Confirmación de Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "105656435"
---
# <a name="ack-for-create-session"></a><span data-ttu-id="5fd73-104">Confirmación para Create-Session</span><span class="sxs-lookup"><span data-stu-id="5fd73-104">Ack for Create-Session</span></span>

<span data-ttu-id="5fd73-105">Use el paquete **de confirmación para creación de sesión** para confirmar la solicitud de [**creación de sesión**](create-session.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="5fd73-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="5fd73-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="5fd73-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="5fd73-107"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="5fd73-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-108">Reemplace Reason-Code por el código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="5fd73-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="5fd73-109">En la tabla siguiente se muestran los códigos de motivo típicos para una respuesta a una solicitud [**de creación de sesión**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd73-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="5fd73-110">Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="5fd73-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="5fd73-111">Código del motivo</span><span class="sxs-lookup"><span data-stu-id="5fd73-111">Reason code</span></span>    | <span data-ttu-id="5fd73-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fd73-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd73-113">200</span><span class="sxs-lookup"><span data-stu-id="5fd73-113">200</span></span><br/> | <span data-ttu-id="5fd73-114">Aceptar.</span><span class="sxs-lookup"><span data-stu-id="5fd73-114">OK.</span></span> <span data-ttu-id="5fd73-115">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="5fd73-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="5fd73-116">201</span><span class="sxs-lookup"><span data-stu-id="5fd73-116">201</span></span><br/> | <span data-ttu-id="5fd73-117">Creado.</span><span class="sxs-lookup"><span data-stu-id="5fd73-117">Created.</span></span> <span data-ttu-id="5fd73-118">Se creó la sesión.</span><span class="sxs-lookup"><span data-stu-id="5fd73-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="5fd73-119">403</span><span class="sxs-lookup"><span data-stu-id="5fd73-119">403</span></span><br/> | <span data-ttu-id="5fd73-120">Prohibido.</span><span class="sxs-lookup"><span data-stu-id="5fd73-120">Forbidden.</span></span> <span data-ttu-id="5fd73-121">No se permite al usuario cargar archivos en la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="5fd73-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="5fd73-122">404</span><span class="sxs-lookup"><span data-stu-id="5fd73-122">404</span></span><br/> | <span data-ttu-id="5fd73-123">Not Found.</span><span class="sxs-lookup"><span data-stu-id="5fd73-123">Not Found.</span></span> <span data-ttu-id="5fd73-124">La dirección URL especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="5fd73-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="5fd73-125">409</span><span class="sxs-lookup"><span data-stu-id="5fd73-125">409</span></span><br/> | <span data-ttu-id="5fd73-126">Conflicto.</span><span class="sxs-lookup"><span data-stu-id="5fd73-126">Conflict.</span></span> <span data-ttu-id="5fd73-127">El archivo existe en el servidor y no se puede sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="5fd73-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="5fd73-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción</span><span class="sxs-lookup"><span data-stu-id="5fd73-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-129">Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo.</span><span class="sxs-lookup"><span data-stu-id="5fd73-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="5fd73-130">Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.</span><span class="sxs-lookup"><span data-stu-id="5fd73-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="5fd73-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-132">Identifica este paquete de respuesta como un paquete de confirmación.</span><span class="sxs-lookup"><span data-stu-id="5fd73-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>Protocolo BITS</span><span class="sxs-lookup"><span data-stu-id="5fd73-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-134">GUID de cadena que identifica el protocolo que el servidor desea usar para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="5fd73-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="5fd73-135">Reemplace {GUID} por el identificador de protocolo de la lista de protocolos que el cliente incluye en la solicitud de [**creación de sesión**](create-session.md) ; el encabezado BITS compatible-protocolo contiene la lista.</span><span class="sxs-lookup"><span data-stu-id="5fd73-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="5fd73-136">Incluya este encabezado solo si el código de motivo es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="5fd73-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS</span><span class="sxs-lookup"><span data-stu-id="5fd73-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-138">GUID de cadena que identifica esta sesión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="5fd73-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="5fd73-139">Reemplace {GUID} por el identificador de sesión que el cliente envía en todos los paquetes de solicitud posteriores.</span><span class="sxs-lookup"><span data-stu-id="5fd73-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="5fd73-140">BITS usa un GUID para identificar la sesión, pero puede usar cualquier cadena HTTP-legal de hasta 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5fd73-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-identificador de host</span><span class="sxs-lookup"><span data-stu-id="5fd73-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fd73-142">Optional.</span></span> <span data-ttu-id="5fd73-143">Incluya este encabezado solo si se ha establecido la [propiedad de extensión de IIS de bits](bits-iis-extension-properties.md), BITSHostId.</span><span class="sxs-lookup"><span data-stu-id="5fd73-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="5fd73-144">Reemplace PublicHostName por el nombre del servidor o la dirección IP de la propiedad BITSHostId.</span><span class="sxs-lookup"><span data-stu-id="5fd73-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="5fd73-145">El cliente debe reemplazar la parte del servidor de la dirección URL remota en todos los paquetes posteriores.</span><span class="sxs-lookup"><span data-stu-id="5fd73-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="5fd73-146">Si el cliente no especifica este nombre de host en los paquetes posteriores, es posible que el trabajo se inicie de nuevo en otro servidor de la granja, lo que deja un archivo de carga parcial en el servidor anterior.</span><span class="sxs-lookup"><span data-stu-id="5fd73-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-host-ID-reserva-timeout</span><span class="sxs-lookup"><span data-stu-id="5fd73-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fd73-148">Optional.</span></span> <span data-ttu-id="5fd73-149">Incluya este encabezado solo si se especifica el encabezado BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="5fd73-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="5fd73-150">Reemplace timeout por el valor de tiempo de espera de la propiedad BITSHostIdFallbackTimeout.</span><span class="sxs-lookup"><span data-stu-id="5fd73-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="5fd73-151">La propiedad BITSHostIdFallbackTimeout es una de las [propiedades de extensión de IIS de bits](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5fd73-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="5fd73-152">El cliente utiliza el período de tiempo de espera para determinar cuánto tiempo intenta volver a conectarse al nombre de servidor especificado en el encabezado BITS-host-ID antes de revertir al nombre de host especificado en el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5fd73-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="5fd73-153">El temporizador comienza cuando BITS no puede conectarse al servidor BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="5fd73-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="5fd73-154">El temporizador se restablece cuando se restaura una conexión al servidor.</span><span class="sxs-lookup"><span data-stu-id="5fd73-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="5fd73-155">Si no se especifica un período de tiempo de espera, el cliente nunca revierte al nombre de host especificado en el nombre de archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="5fd73-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Aceptar: codificación</span><span class="sxs-lookup"><span data-stu-id="5fd73-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-157">Identifica el esquema de codificación que se va a utilizar en los fragmentos enviados al servidor.</span><span class="sxs-lookup"><span data-stu-id="5fd73-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="5fd73-158">El paquete de fragmento contiene el fragmento codificado en el cuerpo del paquete.</span><span class="sxs-lookup"><span data-stu-id="5fd73-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="5fd73-159">El servidor BITS requiere codificación de identidad (texto sin formato).</span><span class="sxs-lookup"><span data-stu-id="5fd73-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="5fd73-160">Incluya este encabezado solo si el código de motivo es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="5fd73-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido</span><span class="sxs-lookup"><span data-stu-id="5fd73-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-162">Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5fd73-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="5fd73-163">Obligatorio incluso si el cuerpo de la respuesta no incluye contenido.</span><span class="sxs-lookup"><span data-stu-id="5fd73-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BIT-error-código</span><span class="sxs-lookup"><span data-stu-id="5fd73-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-165">Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del servidor.</span><span class="sxs-lookup"><span data-stu-id="5fd73-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="5fd73-166">Incluya este encabezado solo si Reason-Code no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="5fd73-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="5fd73-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-error-contexto</span><span class="sxs-lookup"><span data-stu-id="5fd73-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="5fd73-168">Reemplace error-context por un número hexadecimal que representa el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="5fd73-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="5fd73-169">Especifique el número hexadecimal del [**\_ \_ \_ \_ archivo remoto de contexto de error de BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0X5) si el servidor ha generado el error.</span><span class="sxs-lookup"><span data-stu-id="5fd73-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="5fd73-170">En caso contrario, especifique el número hexadecimal de la **\_ \_ \_ \_ aplicación remota de contexto de error de BG** (0X7) si el error fue generado por la aplicación a la que se pasa el archivo de carga.</span><span class="sxs-lookup"><span data-stu-id="5fd73-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="5fd73-171">Incluya este encabezado solo si el código de motivo no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="5fd73-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5fd73-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fd73-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd73-173">**Crear sesión**</span><span class="sxs-lookup"><span data-stu-id="5fd73-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





