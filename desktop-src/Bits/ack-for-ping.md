---
title: Confirmación del ping
description: Use el paquete de confirmación de ping para confirmar la solicitud de ping del cliente.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Confirmación de los BITS de ping
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103995720"
---
# <a name="ack-for-ping"></a><span data-ttu-id="340d2-104">Confirmación del ping</span><span class="sxs-lookup"><span data-stu-id="340d2-104">Ack for Ping</span></span>

<span data-ttu-id="340d2-105">Use el paquete **de confirmación de ping** para confirmar la solicitud de [**ping**](ping.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="340d2-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="340d2-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="340d2-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="340d2-107"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="340d2-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="340d2-108">Reemplace Reason-Code por el código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="340d2-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="340d2-109">Por ejemplo, establezca Reason-Code en 200 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="340d2-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="340d2-110">Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="340d2-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="340d2-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción</span><span class="sxs-lookup"><span data-stu-id="340d2-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="340d2-112">Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo.</span><span class="sxs-lookup"><span data-stu-id="340d2-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="340d2-113">Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.</span><span class="sxs-lookup"><span data-stu-id="340d2-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="340d2-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="340d2-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="340d2-115">Identifica este paquete de respuesta como un paquete de confirmación.</span><span class="sxs-lookup"><span data-stu-id="340d2-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="340d2-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido</span><span class="sxs-lookup"><span data-stu-id="340d2-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="340d2-117">Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="340d2-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="340d2-118">Obligatorio incluso si el cuerpo de la respuesta no incluye contenido.</span><span class="sxs-lookup"><span data-stu-id="340d2-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="340d2-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BIT-error-código</span><span class="sxs-lookup"><span data-stu-id="340d2-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="340d2-120">Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del servidor.</span><span class="sxs-lookup"><span data-stu-id="340d2-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="340d2-121">Incluya este encabezado solo si Reason-Code no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="340d2-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="340d2-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-error-contexto</span><span class="sxs-lookup"><span data-stu-id="340d2-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="340d2-123">Reemplace error-context por un número hexadecimal que representa el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="340d2-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="340d2-124">Especifique el número hexadecimal del [**\_ \_ \_ \_ archivo remoto de contexto de error de BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0X5) si el servidor ha generado el error.</span><span class="sxs-lookup"><span data-stu-id="340d2-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="340d2-125">En caso contrario, especifique el número hexadecimal de la **\_ \_ \_ \_ aplicación remota de contexto de error de BG** (0X7) si el error fue generado por la aplicación a la que se pasa el archivo de carga.</span><span class="sxs-lookup"><span data-stu-id="340d2-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="340d2-126">Incluya este encabezado solo si el código de motivo no es 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="340d2-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="340d2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="340d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340d2-128">**Ping**</span><span class="sxs-lookup"><span data-stu-id="340d2-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




