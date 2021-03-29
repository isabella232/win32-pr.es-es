---
title: Close-Session
description: Use el paquete de Close-Session para indicar al servidor BITS que la carga de archivos se ha completado y para finalizar la sesión.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103903966"
---
# <a name="close-session"></a><span data-ttu-id="fa667-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="fa667-104">Close-Session</span></span>

<span data-ttu-id="fa667-105">Use el paquete **de sesión de cierre** para indicar al servidor bits que la carga de archivos se ha completado y para finalizar la sesión.</span><span class="sxs-lookup"><span data-stu-id="fa667-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="fa667-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="fa667-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="fa667-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post bits</span><span class="sxs-lookup"><span data-stu-id="fa667-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="fa667-108">Verbo específico de BITS que identifica este paquete en el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="fa667-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="fa667-109">Reemplace Remote-URL por el URI absoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="fa667-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="fa667-110">Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="fa667-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="fa667-111">Para conocer las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-host-ID en el paquete de [**creación de sesión**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="fa667-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="fa667-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="fa667-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="fa667-113">Identifica este paquete de solicitud como un paquete de Close-Session.</span><span class="sxs-lookup"><span data-stu-id="fa667-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="fa667-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS</span><span class="sxs-lookup"><span data-stu-id="fa667-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="fa667-115">GUID de cadena que identifica la sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fa667-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="fa667-116">Reemplace {GUID} por el identificador de sesión que devuelve el servidor en el paquete de respuesta [**de confirmación para creación de sesión**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="fa667-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa667-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa667-117">Remarks</span></span>

<span data-ttu-id="fa667-118">El servidor BITS libera todos los recursos y elimina todos los archivos temporales cuando recibe este paquete.</span><span class="sxs-lookup"><span data-stu-id="fa667-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="fa667-119">En el caso de los trabajos de carga y respuesta, debe descargar la respuesta antes de enviar la **sesión de cierre**.</span><span class="sxs-lookup"><span data-stu-id="fa667-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="fa667-120">De lo contrario, se pierde la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa667-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="fa667-121">Si envía este paquete antes de cargar todos los fragmentos, se elimina el archivo de carga; no se puede cargar un archivo parcial.</span><span class="sxs-lookup"><span data-stu-id="fa667-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa667-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa667-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa667-123">**Confirmación de cierre de sesión**</span><span class="sxs-lookup"><span data-stu-id="fa667-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="fa667-124">**Cancelar sesión**</span><span class="sxs-lookup"><span data-stu-id="fa667-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="fa667-125">**Crear sesión**</span><span class="sxs-lookup"><span data-stu-id="fa667-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




