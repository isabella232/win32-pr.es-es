---
description: Necesidades de rendimiento de los usuarios y administradores con aplicaciones de Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Necesidades de rendimiento: usuarios y administradores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082112"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="2d838-103">Necesidades de rendimiento: usuarios y administradores</span><span class="sxs-lookup"><span data-stu-id="2d838-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="2d838-104">Los usuarios juzgan el rendimiento de la aplicación por su experiencia:</span><span class="sxs-lookup"><span data-stu-id="2d838-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="2d838-105">¿La aplicación debe responder rápidamente?</span><span class="sxs-lookup"><span data-stu-id="2d838-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="2d838-106">¿Se muestra un icono de reloj de arena mientras se realizan las operaciones en segundo plano?</span><span class="sxs-lookup"><span data-stu-id="2d838-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="2d838-107">¿La aplicación se inicia y se cierra rápidamente?</span><span class="sxs-lookup"><span data-stu-id="2d838-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="2d838-108">¿Los errores se controlan de forma comprensible?</span><span class="sxs-lookup"><span data-stu-id="2d838-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="2d838-109">En Resumen, los usuarios quieren que las aplicaciones sean rápidas y predecibles.</span><span class="sxs-lookup"><span data-stu-id="2d838-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="2d838-110">Por el contrario, los administradores suelen juzgar el rendimiento de una aplicación en la eficacia con la que usan los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="2d838-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="2d838-111">Los administradores pueden solicitar:</span><span class="sxs-lookup"><span data-stu-id="2d838-111">Administrators may ask:</span></span>

-   <span data-ttu-id="2d838-112">¿La aplicación tiene poca sobrecarga y un uso eficaz de la red?</span><span class="sxs-lookup"><span data-stu-id="2d838-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="2d838-113">¿Es el número mínimo de conexiones usadas, por lo que mi servidor puede atender tantos usuarios como sea posible?</span><span class="sxs-lookup"><span data-stu-id="2d838-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="2d838-114">¿Estoy llamando constantemente al Departamento de soporte técnico?</span><span class="sxs-lookup"><span data-stu-id="2d838-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="2d838-115">En Resumen, los administradores quieren escalar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2d838-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="2d838-116">Prácticas recomendadas para las necesidades de rendimiento</span><span class="sxs-lookup"><span data-stu-id="2d838-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="2d838-117">Al desarrollar una aplicación de Windows Sockets, estos requisitos de rendimiento se traducen en reglas útiles.</span><span class="sxs-lookup"><span data-stu-id="2d838-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="2d838-118">Hacer que las aplicaciones de red se inicialicen rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2d838-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="2d838-119">La interfaz de usuario no debe esperar las respuestas de red.</span><span class="sxs-lookup"><span data-stu-id="2d838-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="2d838-120">Se pueden realizar algunas tareas antes de que la red esté disponible o sin la red.</span><span class="sxs-lookup"><span data-stu-id="2d838-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="2d838-121">Si la red no responde, es posible que el usuario necesite la interfaz de usuario para operaciones sencillas, como cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2d838-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="2d838-122">No espere a que se cierre la red.</span><span class="sxs-lookup"><span data-stu-id="2d838-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="2d838-123">Las aplicaciones cliente y servidor escritas correctamente administran las desconexiones anuladas correctamente.</span><span class="sxs-lookup"><span data-stu-id="2d838-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="2d838-124">No inicie una operación potencialmente larga, como la sincronización de archivos o carpetas con un servidor, que no se puede interrumpir al apagar.</span><span class="sxs-lookup"><span data-stu-id="2d838-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="2d838-125">Las redes no responden de forma coherente, por lo que incluso las pequeñas operaciones podrían demostrar un tiempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="2d838-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="2d838-126">Proporcionar comentarios positivos para los usuarios, incluidas las indicaciones de progreso y los tiempos de finalización estimados.</span><span class="sxs-lookup"><span data-stu-id="2d838-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="2d838-127">Asegúrese de que haya una interfaz de usuario con capacidad de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d838-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="2d838-128">La capacidad de respuesta de las aplicaciones ayuda a eliminar llamadas innecesarias al Departamento</span><span class="sxs-lookup"><span data-stu-id="2d838-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="2d838-129">Una buena directriz para la respuesta interactiva es de 500 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2d838-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="2d838-130">Los usuarios perciben pausas de más de 500 milisegundos como un retraso en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2d838-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="2d838-131">Las aplicaciones deben responder lo suficiente para proporcionar al usuario confianza sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2d838-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="2d838-132">Examine los errores de red.</span><span class="sxs-lookup"><span data-stu-id="2d838-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="2d838-133">No todos los errores de red son críticos.</span><span class="sxs-lookup"><span data-stu-id="2d838-133">Not all network errors are critical.</span></span> <span data-ttu-id="2d838-134">Por ejemplo, una aplicación que ha recibido o enviado todos sus datos puede omitir los errores al cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="2d838-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="2d838-135">No asuma que la red o el usuario están disponibles; controla los errores sin la intervención del usuario o los omite si los errores no son críticos.</span><span class="sxs-lookup"><span data-stu-id="2d838-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="2d838-136">Una aplicación debe definir sus propios tiempos de espera razonables.</span><span class="sxs-lookup"><span data-stu-id="2d838-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="2d838-137">Por ejemplo, una solicitud de Windows Sockets Connect () puede bloquearse en algunas condiciones durante un máximo de 21 segundos.</span><span class="sxs-lookup"><span data-stu-id="2d838-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="2d838-138">Es posible que las aplicaciones necesiten introducir sus propios tiempos de espera según sea necesario para sus usuarios.</span><span class="sxs-lookup"><span data-stu-id="2d838-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="2d838-139">Minimice la sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="2d838-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="2d838-140">El uso del ancho de banda de red es parcialmente mayor que la sobrecarga del protocolo que incurre en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2d838-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="2d838-141">También se trata de la eliminación del tráfico de red innecesario.</span><span class="sxs-lookup"><span data-stu-id="2d838-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="2d838-142">Los protocolos con una sobrecarga de encabezado inferior se pueden usar para transferir datos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2d838-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="2d838-143">Por ejemplo, al enviar cantidades más pequeñas de datos no críticos o repetibles, use UDP en lugar de TCP para reducir la sobrecarga asociada con el establecimiento y el mantenimiento de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2d838-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="2d838-144">Si los mismos datos se deben enviar a varios destinatarios, tenga en cuenta la multidifusión.</span><span class="sxs-lookup"><span data-stu-id="2d838-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="2d838-145">Tenga en cuenta que las aplicaciones UDP no están controladas por flujo. Si se inserta más allá del ancho de banda disponible, se puede producir un error catastrófico en la red.</span><span class="sxs-lookup"><span data-stu-id="2d838-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="2d838-146">La utilidad Netstat se puede usar con las opciones **-e** y **-s** para mostrar las estadísticas de diversos protocolos.</span><span class="sxs-lookup"><span data-stu-id="2d838-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="2d838-147">Conservar recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="2d838-147">Conserve system resources.</span></span>

    <span data-ttu-id="2d838-148">Los recursos del sistema se pueden consumir rápidamente si no se usa la sujeción adecuada.</span><span class="sxs-lookup"><span data-stu-id="2d838-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="2d838-149">Por ejemplo, los sockets y las conexiones TCP consumen recursos.</span><span class="sxs-lookup"><span data-stu-id="2d838-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="2d838-150">No use varias conexiones TCP por cliente, donde una servirá para el propósito de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2d838-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="2d838-151">En el caso de las aplicaciones transaccionales, la buena experiencia del usuario y la utilización de poca red no son objetivos en conflicto.</span><span class="sxs-lookup"><span data-stu-id="2d838-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="2d838-152">La red es un cuello de botella.</span><span class="sxs-lookup"><span data-stu-id="2d838-152">The network is a bottleneck.</span></span> <span data-ttu-id="2d838-153">Las aplicaciones con un uso intensivo de la red dedican más tiempo a esperar y las aplicaciones de red bien escritas están diseñadas para minimizar el tiempo de espera innecesario, tanto para la interfaz de usuario como para las transmisiones de red.</span><span class="sxs-lookup"><span data-stu-id="2d838-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d838-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d838-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d838-155">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="2d838-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="2d838-156">Dimensiones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="2d838-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



