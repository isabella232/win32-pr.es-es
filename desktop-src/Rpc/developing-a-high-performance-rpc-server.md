---
title: Desarrollo de un servidor RPC de alto rendimiento
description: La información de esta sección se aplica a las secuencias de protocolo remoto ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np y a Windows 2000 y Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, desarrollar un servidor de alto rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488158"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="6001d-104">Desarrollo de un servidor RPC de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="6001d-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="6001d-105">La información de esta sección se aplica a las secuencias de protocolo remoto: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**NCACN \_ NP**](/windows/desktop/Midl/ncacn-np)y a Windows 2000 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6001d-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="6001d-106">En esta sección se tratan tres aspectos principales del rendimiento del servidor RPC:</span><span class="sxs-lookup"><span data-stu-id="6001d-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="6001d-107">Latencia y rendimiento de la red</span><span class="sxs-lookup"><span data-stu-id="6001d-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="6001d-108">Escalabilidad</span><span class="sxs-lookup"><span data-stu-id="6001d-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="6001d-109">Sugerencias de rendimiento de RPC varias</span><span class="sxs-lookup"><span data-stu-id="6001d-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="6001d-110">La longitud de la ruta de acceso del código es otra consideración de rendimiento principal de RPC.</span><span class="sxs-lookup"><span data-stu-id="6001d-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="6001d-111">La longitud de la ruta de acceso del código es generalmente entendida y, como la bibliografía y las herramientas están ampliamente disponibles en ese tema, en este artículo no se aborda.</span><span class="sxs-lookup"><span data-stu-id="6001d-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="6001d-112">Una regla de rendimiento general importante y establecida que se debe recordar al considerar el rendimiento de RPC es la siguiente: encontrar el cuello de botella en el sistema y trabajar para resolverlo.</span><span class="sxs-lookup"><span data-stu-id="6001d-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="6001d-113">Es posible que el cuello de botella de la puerta no sea la programación RPC y, en ese caso, el ajuste del rendimiento en RPC no dará lugar a un rendimiento mejorado hasta que se solucione el cuello de botella.</span><span class="sxs-lookup"><span data-stu-id="6001d-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="6001d-114">Por ejemplo, un sistema plagado por la contención de recursos no necesita hacer un uso más eficaz de la red.</span><span class="sxs-lookup"><span data-stu-id="6001d-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="6001d-115">Si el sistema está implementado en varios entornos, es una buena idea asegurarse de que todos los aspectos del mismo estén bien optimizados, ya que los distintos entornos pueden producir cuellos de botella de rendimiento diversos.</span><span class="sxs-lookup"><span data-stu-id="6001d-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 