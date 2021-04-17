---
description: 'Más información acerca de: niveles de seguimiento de Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Niveles de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716627"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="1a24e-103">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="1a24e-104">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="1a24e-105">Hay dos niveles de registro posibles en el seguimiento de Winsock:</span><span class="sxs-lookup"><span data-stu-id="1a24e-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="1a24e-106">Información</span><span class="sxs-lookup"><span data-stu-id="1a24e-106">Information</span></span>
-   <span data-ttu-id="1a24e-107">Verbose</span><span class="sxs-lookup"><span data-stu-id="1a24e-107">Verbose</span></span>

<span data-ttu-id="1a24e-108">El nivel de información realiza el seguimiento de los eventos de creación y cierre de socket, así como cualquier error que se produzca en el socket.</span><span class="sxs-lookup"><span data-stu-id="1a24e-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="1a24e-109">El nivel detallado incluye los eventos de nivel de información y agrega seguimiento adicional para los eventos de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="1a24e-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="1a24e-110">El registro detallado se utilizaría para detectar problemas de daños en el búfer, así como aplicaciones mal escritas.</span><span class="sxs-lookup"><span data-stu-id="1a24e-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="1a24e-111">Se puede usar la información o el nivel detallado con el seguimiento de eventos de red Winsock.</span><span class="sxs-lookup"><span data-stu-id="1a24e-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="1a24e-112">El seguimiento de cambios del catálogo Winsock solo admite el nivel de información.</span><span class="sxs-lookup"><span data-stu-id="1a24e-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="1a24e-113">Seguimiento de eventos de información</span><span class="sxs-lookup"><span data-stu-id="1a24e-113">Information Event Tracing</span></span>

<span data-ttu-id="1a24e-114">En la siguiente lista se detallan las operaciones de socket de eventos de red Winsock cuyo seguimiento se realiza en el nivel de información:</span><span class="sxs-lookup"><span data-stu-id="1a24e-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="1a24e-115">Creación de sockets</span><span class="sxs-lookup"><span data-stu-id="1a24e-115">Socket creation</span></span>

    <span data-ttu-id="1a24e-116">Se ha registrado un evento en la creación de sockets que se puede usar para realizar un seguimiento de la duración de un socket.</span><span class="sxs-lookup"><span data-stu-id="1a24e-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="1a24e-117">Estos eventos también incluyen sockets creados al aceptar conexiones en un socket de escucha.</span><span class="sxs-lookup"><span data-stu-id="1a24e-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="1a24e-118">Bind</span><span class="sxs-lookup"><span data-stu-id="1a24e-118">Bind</span></span>

    <span data-ttu-id="1a24e-119">La dirección IP local se registra para ayudar a correlacionar la información de seguimiento de Winsock con las llamadas de socket de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a24e-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="1a24e-120">Conectar</span><span class="sxs-lookup"><span data-stu-id="1a24e-120">Connect</span></span>

    <span data-ttu-id="1a24e-121">La dirección IP remota del socket conectado se registra para ayudar a correlacionar la información de seguimiento de Winsock con las llamadas de socket de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a24e-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="1a24e-122">Anulaciones y cancelaciones iniciadas por Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="1a24e-123">Cada vez que Winsock anula o cancela activamente una solicitud, se registra el evento.</span><span class="sxs-lookup"><span data-stu-id="1a24e-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="1a24e-124">Restablecimientos iniciados por transporte</span><span class="sxs-lookup"><span data-stu-id="1a24e-124">Transport initiated resets</span></span>

    <span data-ttu-id="1a24e-125">Cada vez que el transporte subyacente indica que se ha restablecido una conexión, se registra el evento.</span><span class="sxs-lookup"><span data-stu-id="1a24e-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="1a24e-126">Errores de envío y recepción</span><span class="sxs-lookup"><span data-stu-id="1a24e-126">Send and receive errors</span></span>

    <span data-ttu-id="1a24e-127">Siempre que se produce un error en una llamada de envío o recepción al transporte subyacente, se registra el evento.</span><span class="sxs-lookup"><span data-stu-id="1a24e-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="1a24e-128">Desconectar socket y cerrar</span><span class="sxs-lookup"><span data-stu-id="1a24e-128">Socket disconnect and close</span></span>

    <span data-ttu-id="1a24e-129">Se registra un evento cuando se cierra un identificador de socket.</span><span class="sxs-lookup"><span data-stu-id="1a24e-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="1a24e-130">Seguimiento detallado de eventos</span><span class="sxs-lookup"><span data-stu-id="1a24e-130">Verbose Event Tracing</span></span>

<span data-ttu-id="1a24e-131">Se realiza un seguimiento de todos los eventos de información en el nivel detallado.</span><span class="sxs-lookup"><span data-stu-id="1a24e-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="1a24e-132">En la siguiente lista se detallan las operaciones adicionales de socket de eventos de red Winsock cuyo seguimiento se realiza en el nivel detallado:</span><span class="sxs-lookup"><span data-stu-id="1a24e-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="1a24e-133">Búferes de envío y recepción</span><span class="sxs-lookup"><span data-stu-id="1a24e-133">Send and receive buffers</span></span>

    <span data-ttu-id="1a24e-134">Los eventos se registran en las direcciones de búfer de usuario y las longitudes cuando las llamadas de envío y recepción se publican en Winsock, así como cuando se completan estas llamadas.</span><span class="sxs-lookup"><span data-stu-id="1a24e-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="1a24e-135">Esto resulta útil para diagnosticar problemas de reutilización de búferes, así como un uso ineficaz de los búferes.</span><span class="sxs-lookup"><span data-stu-id="1a24e-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="1a24e-136">Opciones de socket</span><span class="sxs-lookup"><span data-stu-id="1a24e-136">Socket options</span></span>

    <span data-ttu-id="1a24e-137">Un evento se registra cuando una aplicación cambia determinados valores de opción de socket.</span><span class="sxs-lookup"><span data-stu-id="1a24e-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="1a24e-138">Algunas de las opciones registradas incluyen \_ SNDBUF, por lo que \_ RCVBUF, SiO \_ habilitan la \_ \_ puesta en cola circular y FIONBIO.</span><span class="sxs-lookup"><span data-stu-id="1a24e-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="1a24e-139">WSAPoll y SELECT</span><span class="sxs-lookup"><span data-stu-id="1a24e-139">WSAPoll and select</span></span>

    <span data-ttu-id="1a24e-140">Se registra un evento del uso de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) de una aplicación y se [**seleccionan**](/windows/desktop/api/Winsock2/nf-winsock2-select) llamadas que se pueden usar para encontrar cuellos de botella de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1a24e-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="1a24e-141">Anulaciones y cancelaciones iniciadas por Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="1a24e-142">Cada vez que Winsock anula o cancela activamente una solicitud, se registra el evento.</span><span class="sxs-lookup"><span data-stu-id="1a24e-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="1a24e-143">Máscara de eventos</span><span class="sxs-lookup"><span data-stu-id="1a24e-143">Event mask</span></span>

    <span data-ttu-id="1a24e-144">Se registra un evento de la máscara de eventos que una aplicación registra para usar la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="1a24e-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="1a24e-145">Datagrama</span><span class="sxs-lookup"><span data-stu-id="1a24e-145">Datagram</span></span>

    <span data-ttu-id="1a24e-146">Se registra un evento cada vez que llega un datagrama y no hay espacio en el búfer en el que copiarlo.</span><span class="sxs-lookup"><span data-stu-id="1a24e-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a24e-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a24e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a24e-148">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="1a24e-149">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="1a24e-150">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="1a24e-151">Detalles de seguimiento de eventos de red Winsock</span><span class="sxs-lookup"><span data-stu-id="1a24e-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
