---
title: Cancel-Session
description: Use el paquete de Cancel-Session para finalizar la sesión de carga con el servidor BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105656297"
---
# <a name="cancel-session"></a><span data-ttu-id="d7bbd-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="d7bbd-104">Cancel-Session</span></span>

<span data-ttu-id="d7bbd-105">Use el paquete **de cancelación de sesión** para finalizar la sesión de carga con el servidor bits.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="d7bbd-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="d7bbd-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="d7bbd-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post bits</span><span class="sxs-lookup"><span data-stu-id="d7bbd-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="d7bbd-108">Verbo específico de BITS que identifica este paquete en el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="d7bbd-109">Reemplace Remote-URL por el URI absoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="d7bbd-110">Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="d7bbd-111">Para conocer las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-host-ID en el paquete de [**creación de sesión**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bbd-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="d7bbd-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="d7bbd-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="d7bbd-113">Identifica este paquete de solicitud como un paquete de Cancel-Session.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="d7bbd-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS</span><span class="sxs-lookup"><span data-stu-id="d7bbd-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="d7bbd-115">GUID de cadena que identifica la sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="d7bbd-116">Reemplace {GUID} por el identificador de sesión que devuelve el servidor en el paquete de respuesta [**de confirmación para creación de sesión**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bbd-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7bbd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7bbd-117">Remarks</span></span>

<span data-ttu-id="d7bbd-118">Este paquete cancela un trabajo de carga si se envía antes de que se envíe el último fragmento.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="d7bbd-119">Cancel-Session no tiene ningún efecto en un archivo cuyo último fragmento ya se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="d7bbd-120">Cuando el servidor BITS recibe el último fragmento, escribe el archivo en su destino final y, en el caso de una respuesta de carga, envía el archivo a la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="d7bbd-121">En el caso de la respuesta de carga, el paquete de Cancel-Session cancela la parte de respuesta de un trabajo de carga y respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="d7bbd-122">El servidor BITS libera todos los recursos y elimina todos los archivos temporales cuando recibe este paquete.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="d7bbd-123">El cliente de BITS envía este paquete cuando el usuario cancela el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7bbd-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7bbd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7bbd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bbd-125">**Confirmación de creación: sesión**</span><span class="sxs-lookup"><span data-stu-id="d7bbd-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="d7bbd-126">**Sesión de cierre**</span><span class="sxs-lookup"><span data-stu-id="d7bbd-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




