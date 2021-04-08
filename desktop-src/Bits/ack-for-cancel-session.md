---
title: Confirmación para Cancel-Session
description: Use la confirmación de Cancel-Session paquete para confirmar la solicitud de Cancel-Session del cliente. El servidor envía la confirmación después de liberar todos los recursos asociados a la sesión de carga.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Confirmación de Cancel-Session BITS
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078576"
---
# <a name="ack-for-cancel-session"></a><span data-ttu-id="5125e-105">Confirmación para Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="5125e-105">Ack for Cancel-Session</span></span>

<span data-ttu-id="5125e-106">Use el paquete **ACK para cancelar sesión** para confirmar la solicitud de [**cancelación de sesión**](cancel-session.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="5125e-106">Use the **Ack for Cancel-Session** packet to acknowledge the client's [**Cancel-Session**](cancel-session.md) request.</span></span> <span data-ttu-id="5125e-107">El servidor envía la confirmación después de liberar todos los recursos asociados a la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="5125e-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="5125e-108">Encabezados</span><span class="sxs-lookup"><span data-stu-id="5125e-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="5125e-109"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="5125e-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="5125e-110">Reemplace Reason-Code por el código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="5125e-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="5125e-111">Por ejemplo, establezca Reason-Code en 200 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5125e-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="5125e-112">Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="5125e-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="5125e-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción</span><span class="sxs-lookup"><span data-stu-id="5125e-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="5125e-114">Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo.</span><span class="sxs-lookup"><span data-stu-id="5125e-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="5125e-115">Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.</span><span class="sxs-lookup"><span data-stu-id="5125e-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="5125e-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="5125e-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="5125e-117">Identifica este paquete de respuesta como un paquete de confirmación.</span><span class="sxs-lookup"><span data-stu-id="5125e-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="5125e-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS</span><span class="sxs-lookup"><span data-stu-id="5125e-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="5125e-119">GUID de cadena que identifica la sesión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="5125e-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="5125e-120">Reemplace {GUID} por el identificador de sesión que el cliente envió en el paquete de solicitud [**de cancelación de sesión**](cancel-session.md) .</span><span class="sxs-lookup"><span data-stu-id="5125e-120">Replace {guid} with the session identifier that the client sent in the [**Cancel-Session**](cancel-session.md) request packet.</span></span> <span data-ttu-id="5125e-121">Si no reconoce el identificador de sesión, establezca el encabezado BITS-error-código en la sesión de \_ BG \_ E \_ no \_ encontrada.</span><span class="sxs-lookup"><span data-stu-id="5125e-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="5125e-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido</span><span class="sxs-lookup"><span data-stu-id="5125e-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="5125e-123">Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5125e-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="5125e-124">Obligatorio incluso si el cuerpo de la respuesta no incluye contenido.</span><span class="sxs-lookup"><span data-stu-id="5125e-124">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="5125e-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BIT-error-código</span><span class="sxs-lookup"><span data-stu-id="5125e-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="5125e-126">Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del servidor.</span><span class="sxs-lookup"><span data-stu-id="5125e-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="5125e-127">Incluya solo este encabezado si Reason-Code no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="5125e-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="5125e-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-error-contexto</span><span class="sxs-lookup"><span data-stu-id="5125e-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="5125e-129">Reemplace error-context por un número hexadecimal que representa el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="5125e-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="5125e-130">Especifique el número hexadecimal de [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0X5) si el servidor ha generado el error.</span><span class="sxs-lookup"><span data-stu-id="5125e-130">Specify the hexadecimal number for [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="5125e-131">En caso contrario, especifique el número hexadecimal de la **\_ \_ \_ \_ aplicación remota de contexto de error de BG** (0X7) si el error fue generado por la aplicación a la que se pasa el archivo de carga.</span><span class="sxs-lookup"><span data-stu-id="5125e-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="5125e-132">Incluya este encabezado solo si el código de motivo no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="5125e-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5125e-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5125e-133">Remarks</span></span>

<span data-ttu-id="5125e-134">El cliente de BITS reenvía el paquete de [**cancelación de sesión**](cancel-session.md) si el código de motivo está en el intervalo de 500 a 599, a menos que el encabezado bits-error-Code esté presente con un valor de la \_ sesión BG E \_ \_ no \_ se encuentre.</span><span class="sxs-lookup"><span data-stu-id="5125e-134">The BITS client resends the [**Cancel-Session**](cancel-session.md) packet if the reason-code is in the range from 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="5125e-135">El cliente no volverá a intentarlo por los códigos de motivo 100 a 499.</span><span class="sxs-lookup"><span data-stu-id="5125e-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="5125e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5125e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5125e-137">**Confirmación de cierre de sesión**</span><span class="sxs-lookup"><span data-stu-id="5125e-137">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="5125e-138">**Cancelar sesión**</span><span class="sxs-lookup"><span data-stu-id="5125e-138">**Cancel-Session**</span></span>](cancel-session.md)
</dt> </dl>

 

 




