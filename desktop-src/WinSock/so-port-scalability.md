---
description: Habilita la escalabilidad del puerto local para un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154247"
---
# <a name="so_port_scalability"></a><span data-ttu-id="44583-103">\_ \_ escalabilidad de puertos</span><span class="sxs-lookup"><span data-stu-id="44583-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="44583-104">La opción de socket de **\_ \_ escalabilidad de puertos** permite habilitar la escalabilidad del puerto local para un socket.</span><span class="sxs-lookup"><span data-stu-id="44583-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="44583-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_ \_ escalabilidad de puertos**</span><span class="sxs-lookup"><span data-stu-id="44583-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44583-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="44583-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="44583-107">La opción de socket de **\_ \_ escalabilidad de puertos** permite maximizar la escalabilidad del puerto local al permitir que la asignación de puertos se maximice asignando puertos comodín varias veces para distintos pares de puertos de direcciones locales en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="44583-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44583-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44583-108">Remarks</span></span>

<span data-ttu-id="44583-109">Nota: en plataformas en las que \_ \_ se admiten tanto la escalabilidad de puertos como la \_ reutilización de \_ UNICASTPORT, es preferible usar \_ \_ UNICASTPORT.</span><span class="sxs-lookup"><span data-stu-id="44583-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="44583-110">Los entornos de servidor proxy tienen problemas de escalabilidad debido a la disponibilidad limitada del puerto local.</span><span class="sxs-lookup"><span data-stu-id="44583-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="44583-111">Una manera de solucionar esto es agregar más direcciones IP a la máquina.</span><span class="sxs-lookup"><span data-stu-id="44583-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="44583-112">Sin embargo, de forma predeterminada, los puertos comodín usados con la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) se limitan al tamaño del intervalo de puertos dinámicos en el equipo local (hasta 64 000 puertos, pero normalmente menos) independientemente del número de direcciones IP en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="44583-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="44583-113">Para evitar esto, es necesario que la aplicación mantenga su propio grupo de puertos con la reserva de puertos o mediante la heurística.</span><span class="sxs-lookup"><span data-stu-id="44583-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="44583-114">Para evitar que todas las aplicaciones que requieran escalabilidad administren su propio grupo de puertos y para permitir una mayor escalabilidad, al mismo tiempo que se mantiene la compatibilidad de las aplicaciones, Windows Server 2008 presentó la opción de socket de **\_ \_ escalabilidad de puertos** para ayudar a maximizar la asignación de puertos comodín.</span><span class="sxs-lookup"><span data-stu-id="44583-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="44583-115">La asignación de puertos se maximiza permitiendo que una aplicación asigne puertos comodín para cada par de puerto y dirección local únicos.</span><span class="sxs-lookup"><span data-stu-id="44583-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="44583-116">Por tanto, si un equipo local tiene cuatro direcciones IP, se pueden asignar hasta 256 K puertos comodín (64 K puertos x 4 direcciones IP) mediante solicitudes de función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) comodín.</span><span class="sxs-lookup"><span data-stu-id="44583-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="44583-117">Cuando se establece la opción de socket de **\_ \_ escalabilidad de puertos** en un socket y se realiza una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) para una dirección y un puerto comodín especificados (el parámetro *Name* se establece con una dirección específica y un puerto 0), Winsock asignará un puerto para la dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="44583-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="44583-118">Esta asignación se basará en todas las direcciones IP y puertos posibles y por dirección en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="44583-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="44583-119">Si se adquiere un puerto comodín con la opción de **\_ \_ escalabilidad de puertos** , ese puerto no se puede asignar a otro socket sin la opción de **\_ \_ escalabilidad de puertos** .</span><span class="sxs-lookup"><span data-stu-id="44583-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="44583-120">Esta restricción se aplica para evitar los problemas de compatibilidad con versiones anteriores de las aplicaciones que suponen que no se puede volver a usar un puerto local comodín.</span><span class="sxs-lookup"><span data-stu-id="44583-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="44583-121">Tenga en cuenta que esto significa que las aplicaciones que adquieren un gran número de puertos mediante la **\_ \_ escalabilidad del puerto** pueden privar a las aplicaciones heredadas de los puertos.</span><span class="sxs-lookup"><span data-stu-id="44583-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="44583-122">Si se han adquirido todos los puertos efímeros disponibles para al menos una dirección con la **\_ \_ escalabilidad de puertos** , no se pueden realizar más asignaciones de Puerto comodín sin la opción de socket.</span><span class="sxs-lookup"><span data-stu-id="44583-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="44583-123">Para que surta efecto, se debe establecer la opción de **\_ \_ escalabilidad de puertos para que** se llame a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="44583-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="44583-124">A continuación se muestra un ejemplo de cómo se utilizaría en un equipo con dos direcciones:</span><span class="sxs-lookup"><span data-stu-id="44583-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="44583-125">Un proceso llama a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) para crear un socket.</span><span class="sxs-lookup"><span data-stu-id="44583-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="44583-126">Se llama a la función de llamada para [**Habilitar la opción**](/windows/desktop/api/winsock/nf-winsock-setsockopt) de socket de **\_ \_ escalabilidad de puertos** para el socket recién creado.</span><span class="sxs-lookup"><span data-stu-id="44583-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="44583-127">Se llama a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) para realizar un enlace en una de las direcciones IP del equipo local y en el puerto 0.</span><span class="sxs-lookup"><span data-stu-id="44583-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="44583-128">A continuación, se llama a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) para conectarse a una dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="44583-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="44583-129">La aplicación usa el socket según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="44583-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="44583-130">Una función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) se llama mediante el mismo proceso (posiblemente un subproceso diferente) para crear un segundo Socket.</span><span class="sxs-lookup"><span data-stu-id="44583-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="44583-131">Se llama a la función de llamada para [**Habilitar la opción**](/windows/desktop/api/winsock/nf-winsock-setsockopt) de socket de **\_ \_ escalabilidad de puertos** para el segundo socket recién creado.</span><span class="sxs-lookup"><span data-stu-id="44583-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="44583-132">Se llama a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) con la segunda dirección IP y el puerto 0 del equipo local.</span><span class="sxs-lookup"><span data-stu-id="44583-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="44583-133">Incluso cuando todos los puertos se han asignado previamente, esta llamada se realiza correctamente porque hay varias direcciones IP disponibles en el equipo local y la opción de socket de **\_ \_ escalabilidad de puertos para que** se haya establecido en ambos Sockets en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="44583-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="44583-134">A continuación, se llama a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) para conectarse a una dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="44583-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="44583-135">La aplicación usa el segundo socket según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="44583-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="44583-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44583-136">Requirements</span></span>



| <span data-ttu-id="44583-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="44583-137">Requirement</span></span> | <span data-ttu-id="44583-138">Value</span><span class="sxs-lookup"><span data-stu-id="44583-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44583-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44583-139">Minimum supported client</span></span><br/> | <span data-ttu-id="44583-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44583-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="44583-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44583-141">Minimum supported server</span></span><br/> | <span data-ttu-id="44583-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="44583-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44583-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44583-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="44583-144"><dt>Ws2def. h</dt></span><span class="sxs-lookup"><span data-stu-id="44583-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44583-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="44583-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44583-146">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="44583-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="44583-147">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="44583-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="44583-148">**\_Opciones de socket de socket sol**</span><span class="sxs-lookup"><span data-stu-id="44583-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="44583-149">**Opciones de socket**</span><span class="sxs-lookup"><span data-stu-id="44583-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




