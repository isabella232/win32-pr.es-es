---
title: Propiedades de Message y Message Queue
description: Un mensaje tiene propiedades, que especifican una etiqueta, un cuerpo de mensaje y varias opciones.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357341"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="3f376-103">Propiedades de Message y Message Queue</span><span class="sxs-lookup"><span data-stu-id="3f376-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="3f376-104">Un mensaje tiene propiedades, que especifican una etiqueta, un cuerpo de mensaje y varias opciones.</span><span class="sxs-lookup"><span data-stu-id="3f376-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="3f376-105">Las opciones de propiedad del mensaje pueden incluir la calidad de servicio, la prioridad, el registro en diario, los niveles de privacidad y autenticación, y la duración del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3f376-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="3f376-106">En las aplicaciones de Message Queue Server (no RPC) convencionales, estas propiedades se especifican mediante una llamada a las funciones de la API de MSMQ o a los métodos de objeto COM, que se describen en la documentación del SDK de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="3f376-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="3f376-107">Las aplicaciones cliente RPC pueden establecer determinadas propiedades para llamadas a procedimientos remotos llamando a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) y [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="3f376-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="3f376-108">Una vez establecidas, las propiedades permanecen en vigor para cada mensaje hasta que la aplicación cliente las restablece.</span><span class="sxs-lookup"><span data-stu-id="3f376-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="3f376-109">Una cola de mensajes tiene su propio conjunto de propiedades, además de los de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="3f376-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="3f376-110">Estas propiedades identifican de forma única una cola y definen la clase de servicio que proporciona la cola, los niveles de privacidad y autenticación necesarios para los mensajes de esta cola, y si los mensajes van a formar parte de una transacción distribuida.</span><span class="sxs-lookup"><span data-stu-id="3f376-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="3f376-111">Al igual que con las propiedades del mensaje, se especifican las propiedades de una cola de mensajes mediante una llamada a las funciones de la API de MSMQ o a los métodos de objeto COM, que se describen en la documentación de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="3f376-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="3f376-112">Sin embargo, una aplicación de servidor RPC puede especificar propiedades de su propia cola de recepción cuando llama a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) para establecer el enlace.</span><span class="sxs-lookup"><span data-stu-id="3f376-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 




