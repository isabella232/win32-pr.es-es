---
title: Prácticas recomendadas de equilibrio de carga
description: Prácticas recomendadas de equilibrio de carga
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995476"
---
# <a name="load-balancing-best-practices"></a><span data-ttu-id="0eb01-103">Prácticas recomendadas de equilibrio de carga</span><span class="sxs-lookup"><span data-stu-id="0eb01-103">Load Balancing Best Practices</span></span>

<span data-ttu-id="0eb01-104">Se deben seguir varios procedimientos recomendados al instalar y configurar el equilibrio de carga de RPC.</span><span class="sxs-lookup"><span data-stu-id="0eb01-104">Several best practices should be followed when setting up and configuring RPC Load balancing.</span></span>

<span data-ttu-id="0eb01-105">En primer lugar, se debe establecer la seguridad en las llamadas de libras entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="0eb01-105">First, security should be set on incoming and outgoing LBS calls.</span></span> <span data-ttu-id="0eb01-106">Esto significa que las dos claves del registro de [NoSecurity](configuring-load-balancing.md) opcionales no deben estar presentes o deben establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="0eb01-106">This means both of the optional [NoSecurity](configuring-load-balancing.md) registry keys should either not be present or should be set to zero.</span></span>

<span data-ttu-id="0eb01-107">En segundo lugar, se debe prestar atención a la solución de equilibrio de carga de front-end que se usa junto con la solución de equilibrio de carga de RPC.</span><span class="sxs-lookup"><span data-stu-id="0eb01-107">Second, attention must be paid to the front end load balancing solution used in conjunction with the RPC Load Balancing solution.</span></span> <span data-ttu-id="0eb01-108">Por ejemplo, si el equilibrador de carga de front-end usa el equilibrio de carga de round robin simple, debe existir un número impar de servidores en la granja de servidores.</span><span class="sxs-lookup"><span data-stu-id="0eb01-108">For example, if the front end load balancer uses simple round robin load balancing, an odd number of servers should exist in the server farm.</span></span> <span data-ttu-id="0eb01-109">Esto se hace para mitigar la posibilidad de que todas las conexiones se reenvíen y, por lo tanto, el mismo servidor o servidores los prestan servicio.</span><span class="sxs-lookup"><span data-stu-id="0eb01-109">This is to mitigate the possibility of all connections being forwarded and thus serviced by the same server or servers.</span></span>

<span data-ttu-id="0eb01-110">Por seguridad, suele ser conveniente tener un firewall de control de acceso a los servidores proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="0eb01-110">For security, it is commonly desirable to have a firewall control access to RPC Proxy servers.</span></span> <span data-ttu-id="0eb01-111">Si se emplea una solución de Firewall basada en Puerto, los extremos de RPC deben ser estáticos para limitar el número de puertos que se abren en el firewall.</span><span class="sxs-lookup"><span data-stu-id="0eb01-111">If a port based firewall solution is employed, RPC endpoints must be static in order to limit the number of ports that are opened in the firewall.</span></span> <span data-ttu-id="0eb01-112">En Windows Server 2008 y versiones posteriores de Windows, RPC proporciona un mecanismo para asignar un puerto estático a puntos de conexión dinámicos.</span><span class="sxs-lookup"><span data-stu-id="0eb01-112">On Windows Server 2008 and later versions of Windows, RPC provides a mechanism to assign a static port to dynamic endpoints.</span></span> <span data-ttu-id="0eb01-113">Esto se logra a través de los comandos de Firewall netsh de RPC.</span><span class="sxs-lookup"><span data-stu-id="0eb01-113">This is achieved through the RPC netsh firewall commands.</span></span> <span data-ttu-id="0eb01-114">Un conjunto de comandos de ejemplo para establecer la interfaz lb en el puerto estático de 3010 es:</span><span class="sxs-lookup"><span data-stu-id="0eb01-114">An example set of commands to set the LBS interface to the static port of 3010 is:</span></span>

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

<span data-ttu-id="0eb01-115">El comando RPC netsh se puede usar para establecer un punto de conexión estático para cualquier interfaz dinámica o estática.</span><span class="sxs-lookup"><span data-stu-id="0eb01-115">The RPC netsh command can be used to set a static endpoint for any dynamic or static interface.</span></span> <span data-ttu-id="0eb01-116">Esto resulta útil cuando se restringe el acceso a un equipo que ejecuta una solución de Firewall basada en Puerto.</span><span class="sxs-lookup"><span data-stu-id="0eb01-116">This is useful when restricting access to a machine running a port based firewall solution.</span></span> <span data-ttu-id="0eb01-117">Si se usa la solución de Firewall de Windows, la interfaz RPC puede bloquearse o habilitarse sin tener que asignarla a un puerto específico.</span><span class="sxs-lookup"><span data-stu-id="0eb01-117">If the Windows firewall solution is used, the RPC interface can be blocked or enabled without having to assign it to a specific port.</span></span> <span data-ttu-id="0eb01-118">Para obtener más información, vea la [Referencia del comando RPC netsh firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="0eb01-118">For more information, see the [RPC netsh firewall command reference](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span></span>

 

 