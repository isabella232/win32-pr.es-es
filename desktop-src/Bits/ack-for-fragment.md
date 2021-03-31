---
title: Confirmación para fragmento
description: Use la confirmación para que el paquete de fragmentos confirme la solicitud de fragmento del cliente.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Confirmación para BITS de fragmento
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103995721"
---
# <a name="ack-for-fragment"></a><span data-ttu-id="d0ec5-104">Confirmación para fragmento</span><span class="sxs-lookup"><span data-stu-id="d0ec5-104">Ack for Fragment</span></span>

<span data-ttu-id="d0ec5-105">Use la **confirmación para** que el paquete de fragmentos confirme la solicitud de [**fragmento**](fragment.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="d0ec5-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="d0ec5-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="d0ec5-107"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="d0ec5-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-108">Reemplace Reason-Code por un código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="d0ec5-109">En la tabla siguiente se muestran los códigos de motivo típicos para una respuesta a una solicitud de [**fragmento**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="d0ec5-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="d0ec5-110">Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="d0ec5-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="d0ec5-111">Código del motivo</span><span class="sxs-lookup"><span data-stu-id="d0ec5-111">Reason code</span></span>    | <span data-ttu-id="d0ec5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0ec5-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ec5-113">200</span><span class="sxs-lookup"><span data-stu-id="d0ec5-113">200</span></span><br/> | <span data-ttu-id="d0ec5-114">Aceptar.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-114">OK.</span></span> <span data-ttu-id="d0ec5-115">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="d0ec5-116">416</span><span class="sxs-lookup"><span data-stu-id="d0ec5-116">416</span></span><br/> | <span data-ttu-id="d0ec5-117">Range: no-se puede satisfacer.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="d0ec5-118">El cliente envió un fragmento cuyo intervalo no es contiguo con el fragmento anterior.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d0ec5-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción</span><span class="sxs-lookup"><span data-stu-id="d0ec5-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-120">Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="d0ec5-121">Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="d0ec5-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-123">Identifica este paquete de respuesta como un paquete de confirmación.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-recibido-contenido-intervalo</span><span class="sxs-lookup"><span data-stu-id="d0ec5-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-125">Desplazamiento de base cero al siguiente byte que el servidor espera que el cliente envíe.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="d0ec5-126">Por ejemplo, si el fragmento contenía el intervalo 128 212, debe establecer intervalo en 213.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS</span><span class="sxs-lookup"><span data-stu-id="d0ec5-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-128">GUID de cadena que identifica la sesión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="d0ec5-129">Reemplace {GUID} por el identificador de sesión que el cliente envió en el paquete de solicitud de [**fragmento**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="d0ec5-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="d0ec5-130">Si no reconoce el identificador de sesión, establezca el encabezado BITS-error-código en la sesión de \_ BG \_ E \_ no \_ encontrada.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>Dirección URL de BITS-respuesta</span><span class="sxs-lookup"><span data-stu-id="d0ec5-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-132">Contiene la dirección URL de los datos de respuesta de un trabajo de carga y respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="d0ec5-133">Incluya este encabezado en la respuesta de fragmento final una vez completada la carga y reciba una respuesta de la aplicación de servidor, si procede.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="d0ec5-134">Use el encabezado Content-Range de la solicitud de fragmento para determinar si la carga se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="d0ec5-135">La carga se completa si el desplazamiento final del valor del intervalo es igual al valor de longitud total menos uno.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="d0ec5-136">El servidor BITS envía el archivo de carga a la aplicación de servidor una vez que determina que la carga se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="d0ec5-137">La aplicación de servidor procesa el archivo y genera la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="d0ec5-138">El servidor BITS establece el valor de BITS-reply-URL en la dirección URL del archivo de respuesta de la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido</span><span class="sxs-lookup"><span data-stu-id="d0ec5-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-140">Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="d0ec5-141">La longitud del contenido es obligatoria, incluso si el cuerpo de la respuesta no incluye contenido.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BIT-error-código</span><span class="sxs-lookup"><span data-stu-id="d0ec5-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-143">Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del servidor.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="d0ec5-144">Incluya solo este encabezado si Reason-Code no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-error-contexto</span><span class="sxs-lookup"><span data-stu-id="d0ec5-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="d0ec5-146">Reemplace error-context por un número hexadecimal que representa el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="d0ec5-147">Especifique el número hexadecimal del [**\_ \_ \_ \_ archivo remoto de contexto de error de BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0X5) si el servidor ha generado el error.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="d0ec5-148">En caso contrario, especifique el número hexadecimal de la **\_ \_ \_ \_ aplicación remota de contexto de error de BG** (0X7) si el error fue generado por la aplicación a la que se pasa el archivo de carga.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="d0ec5-149">Incluya este encabezado solo si el código de motivo no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0ec5-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0ec5-150">Remarks</span></span>

<span data-ttu-id="d0ec5-151">Si la sesión es para un trabajo de carga y respuesta, puede haber un retraso antes de que el cliente reciba la confirmación final de la respuesta **de fragmento** .</span><span class="sxs-lookup"><span data-stu-id="d0ec5-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="d0ec5-152">La duración del retraso depende de la cantidad de tiempo que la aplicación de servidor (la aplicación a la que el servidor envía el archivo de carga) tarda en generar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0ec5-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0ec5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ec5-154">**Crear sesión**</span><span class="sxs-lookup"><span data-stu-id="d0ec5-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="d0ec5-155">**Fragmento**</span><span class="sxs-lookup"><span data-stu-id="d0ec5-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





