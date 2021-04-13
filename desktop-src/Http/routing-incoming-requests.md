---
title: Enrutamiento de solicitudes entrantes
description: La API del servidor HTTP mantiene una base de datos de enrutamiento para determinar qué aplicación recibe una solicitud entrante.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421586"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="711ad-103">Enrutamiento de solicitudes entrantes</span><span class="sxs-lookup"><span data-stu-id="711ad-103">Routing Incoming Requests</span></span>

<span data-ttu-id="711ad-104">La API del servidor HTTP mantiene una base de datos de enrutamiento para determinar qué aplicación recibe una solicitud entrante.</span><span class="sxs-lookup"><span data-stu-id="711ad-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="711ad-105">La tabla de enrutamiento se genera a partir de la base de datos de reserva y contiene entradas de reserva, así como registros actuales.</span><span class="sxs-lookup"><span data-stu-id="711ad-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="711ad-106">Cuando se realiza un registro o una reserva, se coloca en el cubo de la base de datos de enrutamiento que corresponde al tipo de host de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="711ad-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="711ad-107">\+ : los registros de puerto se colocan en el cubo "comodín seguro".</span><span class="sxs-lookup"><span data-stu-id="711ad-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="711ad-108">host: los registros de puerto se colocan en el cubo "explícito"</span><span class="sxs-lookup"><span data-stu-id="711ad-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="711ad-109">IP: los registros de puerto se colocan en el cubo "comodín débil de IP enlazada"</span><span class="sxs-lookup"><span data-stu-id="711ad-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="711ad-110">\* : los registros de puerto se colocan en el cubo "comodín débil"</span><span class="sxs-lookup"><span data-stu-id="711ad-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="711ad-111">Estos pasos también hacen referencia al orden en que se procesan las solicitudes HTTP entrantes.</span><span class="sxs-lookup"><span data-stu-id="711ad-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="711ad-112">En primer lugar, se comprueban las reservas de caracteres comodín seguros y, a continuación, se comprueba la reserva explícita seguida del carácter comodín débil y el carácter comodín débil.</span><span class="sxs-lookup"><span data-stu-id="711ad-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="711ad-113">La búsqueda se detiene cuando se encuentra una coincidencia para que no se encuentren los registros en ninguno de los cubos restantes.</span><span class="sxs-lookup"><span data-stu-id="711ad-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="711ad-114">El algoritmo de enrutamiento de la API del servidor HTTP localiza la mejor coincidencia para [UrlPrefix](urlprefix-strings.md) mediante la búsqueda de las entradas de registro y de las entradas de reserva de la base de datos de enrutamiento, comenzando por el depósito de comodín seguro y finalizando con el depósito de comodín débil.</span><span class="sxs-lookup"><span data-stu-id="711ad-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="711ad-115">La mejor coincidencia, dentro de un depósito, es la coincidencia más larga en la parte del URI relativo de UrlPrefix (suponiendo que haya una coincidencia exacta para las partes de host, puerto y esquema de la dirección URL).</span><span class="sxs-lookup"><span data-stu-id="711ad-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="711ad-116">Una vez que se encuentra una coincidencia en un depósito, el algoritmo de enrutamiento detiene su búsqueda y omite todos los depósitos de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="711ad-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="711ad-117">Por ejemplo, considere los siguientes registros (en orden descendente de prioridad en función de los tipos de cubos:</span><span class="sxs-lookup"><span data-stu-id="711ad-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="711ad-118">Registro: `https://+:80/vroot/` está registrado por la aplicación 1</span><span class="sxs-lookup"><span data-stu-id="711ad-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="711ad-119">Registro: `https://adatum.com:80/` está registrado por la aplicación 2</span><span class="sxs-lookup"><span data-stu-id="711ad-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="711ad-120">Registro: `https://\*:80/` está registrado por la aplicación 3</span><span class="sxs-lookup"><span data-stu-id="711ad-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="711ad-121">Una solicitud entrante para `https://adatum.com:80/vroot/subdir/file.htm/` se entrega a la aplicación 1.</span><span class="sxs-lookup"><span data-stu-id="711ad-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="711ad-122">Una solicitud entrante para `https://adatum.com:80/default.htm/` se entrega a la aplicación 2.</span><span class="sxs-lookup"><span data-stu-id="711ad-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="711ad-123">Una solicitud entrante para `https://otheradatum.com:80/file.htm/` se entrega a la aplicación 3.</span><span class="sxs-lookup"><span data-stu-id="711ad-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="711ad-124">Si la mejor coincidencia es una entrada de reserva, significa que la aplicación que debe recibir la solicitud no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="711ad-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="711ad-125">Por ejemplo, considere el registro y la reserva siguientes:</span><span class="sxs-lookup"><span data-stu-id="711ad-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="711ad-126">Registro: `https://\*:80/vroot/` está registrado por la aplicación 1, el usuario A</span><span class="sxs-lookup"><span data-stu-id="711ad-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="711ad-127">Reserva: se `https://adatum.com:80/` ha reservado para el usuario B</span><span class="sxs-lookup"><span data-stu-id="711ad-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="711ad-128">Una solicitud entrante para `https://adatum.com:80/vroot/file.htm/` no se entrega a la aplicación 1 porque la mejor coincidencia conduce a la entrada de reserva para el usuario B. Las reglas de prioridad se aplican en este caso a la reserva que tiene una prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="711ad-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="711ad-129">Si no hay ningún proceso activo que esté autorizado y registrado en las solicitudes de servicio de la dirección URL recibida, la solicitud se rechazará con un código de estado 400 (solicitud incorrecta).</span><span class="sxs-lookup"><span data-stu-id="711ad-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




