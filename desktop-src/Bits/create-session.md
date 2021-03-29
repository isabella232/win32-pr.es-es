---
title: Create-Session
description: Use el paquete de Create-Session para solicitar una sesión de carga con el servidor BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487091"
---
# <a name="create-session"></a><span data-ttu-id="927bd-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="927bd-104">Create-Session</span></span>

<span data-ttu-id="927bd-105">Use el paquete **de creación de sesión** para solicitar una sesión de carga con el servidor bits.</span><span class="sxs-lookup"><span data-stu-id="927bd-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="927bd-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="927bd-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="927bd-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post bits</span><span class="sxs-lookup"><span data-stu-id="927bd-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="927bd-108">Verbo específico de BITS que identifica este paquete en el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="927bd-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="927bd-109">Reemplace Remote-URL por el URI absoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="927bd-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="927bd-110">Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="927bd-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="927bd-111">Para conocer las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="927bd-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="927bd-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="927bd-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="927bd-113">Identifica este paquete de solicitud como un paquete de Create-Session.</span><span class="sxs-lookup"><span data-stu-id="927bd-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="927bd-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS: protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="927bd-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="927bd-115">Lista delimitada por espacios de los protocolos que admite el cliente.</span><span class="sxs-lookup"><span data-stu-id="927bd-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="927bd-116">Use GUID de cadena para identificar los protocolos.</span><span class="sxs-lookup"><span data-stu-id="927bd-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="927bd-117">Especifique la lista en orden de preferencia de más a menos preferida.</span><span class="sxs-lookup"><span data-stu-id="927bd-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="927bd-118">En la tabla siguiente se muestra el protocolo que admite el cliente BITS.</span><span class="sxs-lookup"><span data-stu-id="927bd-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="927bd-119">Reemplace {guid1}... {guidn} con uno o más GUID de cadena de la lista.</span><span class="sxs-lookup"><span data-stu-id="927bd-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="927bd-120">Protocolo</span><span class="sxs-lookup"><span data-stu-id="927bd-120">Protocol</span></span>                                          | <span data-ttu-id="927bd-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="927bd-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="927bd-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span><span class="sxs-lookup"><span data-stu-id="927bd-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="927bd-123">Protocolo de carga de BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="927bd-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="927bd-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="927bd-124">Remarks</span></span>

<span data-ttu-id="927bd-125">Debe enviar un paquete [**ping**](ping.md) para establecer una conexión http antes de enviar el paquete de Create-Session.</span><span class="sxs-lookup"><span data-stu-id="927bd-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="927bd-126">El paquete de Create-Session también puede establecer la conexión; sin embargo, el paquete de Create-Session es menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="927bd-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="927bd-127">El servidor selecciona el protocolo que desea utilizar en la lista que el cliente proporciona en el encabezado BITS-compatible-protocolos.</span><span class="sxs-lookup"><span data-stu-id="927bd-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="927bd-128">El servidor devuelve el protocolo seleccionado en el encabezado BITS-Protocol del paquete de respuesta de [**confirmación de creación de sesión**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="927bd-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="927bd-129">El cliente espera que el servidor devuelva una [**confirmación para el paquete de respuesta de la sesión de creación**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="927bd-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="927bd-130">Si el servidor ha podido establecer una sesión, el cliente utiliza el paquete de solicitud de [**fragmento**](fragment.md) para enviar intervalos del archivo al servidor.</span><span class="sxs-lookup"><span data-stu-id="927bd-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="927bd-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="927bd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927bd-132">**Confirmación de creación: sesión**</span><span class="sxs-lookup"><span data-stu-id="927bd-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="927bd-133">**Fragmento**</span><span class="sxs-lookup"><span data-stu-id="927bd-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="927bd-134">**Ping**</span><span class="sxs-lookup"><span data-stu-id="927bd-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





