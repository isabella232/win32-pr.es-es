---
title: Ping
description: Use el paquete ping para establecer una conexión y negociar la seguridad con el servidor.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Hacer ping de BITS
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "105656301"
---
# <a name="ping"></a><span data-ttu-id="8cb4f-104">Ping</span><span class="sxs-lookup"><span data-stu-id="8cb4f-104">Ping</span></span>

<span data-ttu-id="8cb4f-105">Use el paquete **ping** para establecer una conexión y negociar la seguridad con el servidor.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="8cb4f-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="8cb4f-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="8cb4f-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post bits</span><span class="sxs-lookup"><span data-stu-id="8cb4f-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="8cb4f-108">Verbo específico de BITS que identifica este paquete en el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="8cb4f-109">Reemplace Remote-URL por el URI absoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="8cb4f-110">Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="8cb4f-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="8cb4f-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="8cb4f-112">Identifica este paquete de solicitud como un paquete de ping.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cb4f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cb4f-113">Remarks</span></span>

<span data-ttu-id="8cb4f-114">El paquete **ping** es opcional.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="8cb4f-115">En lugar de enviar un paquete **ping** , puede usar el paquete [**de creación de sesión**](create-session.md) para establecer una conexión y negociar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="8cb4f-116">Sin embargo, es más eficaz usar el paquete **ping** con este fin.</span><span class="sxs-lookup"><span data-stu-id="8cb4f-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cb4f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cb4f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb4f-118">**Confirmación del ping**</span><span class="sxs-lookup"><span data-stu-id="8cb4f-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="8cb4f-119">**Crear sesión**</span><span class="sxs-lookup"><span data-stu-id="8cb4f-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




