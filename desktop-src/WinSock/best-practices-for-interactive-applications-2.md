---
description: En la transformación del código de actualización de la celda de vida, se han descubierto varias instrucciones para escribir aplicaciones de red de alto rendimiento.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Prácticas recomendadas para aplicaciones interactivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715140"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="3bfc1-103">Prácticas recomendadas para aplicaciones interactivas</span><span class="sxs-lookup"><span data-stu-id="3bfc1-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="3bfc1-104">En la transformación del código de actualización de la celda de vida, se han descubierto varias instrucciones para escribir aplicaciones de red de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="3bfc1-105">Algunas de las estrategias generales que se deben aplicar al escribir estos tipos de aplicaciones son:</span><span class="sxs-lookup"><span data-stu-id="3bfc1-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="3bfc1-106">Haga que el flujo de datos sea lo máximo posible, en lugar de pasar por fragmentos.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="3bfc1-107">Use algunas transacciones grandes en lugar de muchas pequeñas.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="3bfc1-108">Las transacciones grandes también se pueden transmitir de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="3bfc1-109">Reconozca que la red es un recurso lento y confiable, y desarrolle cada aplicación para minimizar su dependencia en la red.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="3bfc1-110">Usar una representación bien diseñada de los datos de la red.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="3bfc1-111">La representación de los datos debe ser independiente de la arquitectura del equipo, no contener ninguna FAT y, posiblemente, estar comprimida.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="3bfc1-112">Durante la inicialización y el cierre, no haga que el usuario espere a que la red se inicie o se apague.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="3bfc1-113">La inicialización relacionada con la red puede tardar bastante tiempo.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="3bfc1-114">Separe el código de red no crítico.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="3bfc1-115">Controlar los errores según corresponda.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="3bfc1-116">No todos los errores son críticos.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-116">Not all errors are critical.</span></span> <span data-ttu-id="3bfc1-117">Implementar mecanismos de recuperación y proporcionar comentarios de los usuarios no intrusivos.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="3bfc1-118">Use llamadas a procedimiento remoto (RPC) solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="3bfc1-119">RPC es sincrónico en Windows Me/98 y siempre da como resultado la conversación y los protocolos FAT cuando se usa para enviar pequeñas cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="3bfc1-120">Mida la sobrecarga de la red mediante netstat; es posible que se sorprenda de lo que se revela en las mediciones.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="3bfc1-121">Pruebe la aplicación en una gran variedad de redes, especialmente en redes lentas o propensas a pérdidas.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="3bfc1-122">Las redes LAN inalámbricas, los módems y las redes privadas virtuales (VPN) a través de Internet son buenas redes para las pruebas.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bfc1-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3bfc1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bfc1-124">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="3bfc1-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



