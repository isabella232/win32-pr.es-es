---
title: Paquetes de solicitud de BITS
description: Paquetes de solicitud de BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993977"
---
# <a name="bits-request-packets"></a><span data-ttu-id="247d5-103">Paquetes de solicitud de BITS</span><span class="sxs-lookup"><span data-stu-id="247d5-103">BITS Request Packets</span></span>

<span data-ttu-id="247d5-104">Los paquetes de solicitud describen las solicitudes del cliente.</span><span class="sxs-lookup"><span data-stu-id="247d5-104">Request packets describe client requests.</span></span> <span data-ttu-id="247d5-105">Solo puede haber una solicitud pendiente en un momento dado; debe recibir una [confirmación](bits-response-packets.md) para la solicitud actual del servidor antes de enviar otra solicitud.</span><span class="sxs-lookup"><span data-stu-id="247d5-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="247d5-106">En la tabla siguiente se enumeran los paquetes de solicitud enviados al servidor BITS para los trabajos de carga y de carga y respuesta.</span><span class="sxs-lookup"><span data-stu-id="247d5-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="247d5-107">En la tabla se enumeran los paquetes en la secuencia típica que se envían al servidor.</span><span class="sxs-lookup"><span data-stu-id="247d5-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="247d5-108">Paquete de solicitud</span><span class="sxs-lookup"><span data-stu-id="247d5-108">Request packet</span></span>                       | <span data-ttu-id="247d5-109">Propósito</span><span class="sxs-lookup"><span data-stu-id="247d5-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="247d5-110">Ping</span><span class="sxs-lookup"><span data-stu-id="247d5-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="247d5-111">Establece una conexión y negocia la seguridad con el servidor.</span><span class="sxs-lookup"><span data-stu-id="247d5-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="247d5-112">Crear sesión</span><span class="sxs-lookup"><span data-stu-id="247d5-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="247d5-113">Solicita una sesión de carga con el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="247d5-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="247d5-114">Fragmento</span><span class="sxs-lookup"><span data-stu-id="247d5-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="247d5-115">Envía un fragmento del archivo al servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="247d5-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="247d5-116">El número de solicitudes de fragmentos enviadas depende del tamaño de fragmento que elija y del tamaño del archivo de carga.</span><span class="sxs-lookup"><span data-stu-id="247d5-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="247d5-117">Sesión de cierre</span><span class="sxs-lookup"><span data-stu-id="247d5-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="247d5-118">Finaliza la sesión de carga de archivos con el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="247d5-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="247d5-119">Cancelar sesión</span><span class="sxs-lookup"><span data-stu-id="247d5-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="247d5-120">Finaliza la sesión de carga de archivos con el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="247d5-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="247d5-121">Normalmente, se envía el paquete de Cancel-Session si el usuario canceló el trabajo.</span><span class="sxs-lookup"><span data-stu-id="247d5-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="247d5-122">El paquete Ping es opcional.</span><span class="sxs-lookup"><span data-stu-id="247d5-122">The Ping packet is optional.</span></span> <span data-ttu-id="247d5-123">En lugar de enviar un paquete ping, puede usar el paquete de Create-Session para establecer una conexión y negociar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="247d5-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="247d5-124">Sin embargo, es más eficaz usar el paquete ping con este fin.</span><span class="sxs-lookup"><span data-stu-id="247d5-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




