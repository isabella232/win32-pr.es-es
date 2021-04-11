---
description: El \_ ioctl de \_ \_ ordenación de la lista de direcciones de SiO permite a los desarrolladores de aplicaciones ordenar una lista de direcciones IPv6 e IPv4 de destino para determinar la mejor dirección disponible para establecer una conexión. El \_ \_ ioctl de ordenación de la lista de direcciones \_ de SiO es compatible con Windows XP y versiones posteriores.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Usar SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278785"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="dcffb-104">Usar la \_ ordenación de la lista de direcciones de SiO \_ \_</span><span class="sxs-lookup"><span data-stu-id="dcffb-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="dcffb-105">El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO permite a los desarrolladores de aplicaciones ordenar una lista de direcciones IPv6 e IPv4 de destino para determinar la mejor dirección disponible para establecer una conexión.</span><span class="sxs-lookup"><span data-stu-id="dcffb-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="dcffb-106">El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO es compatible con Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcffb-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="dcffb-107">En Windows Vista y versiones posteriores, la función [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) toma una lista proporcionada de posibles direcciones IP de destino, empareja las direcciones de destino con las direcciones IP locales de la máquina host y ordena los pares según el par de direcciones más adecuado para la comunicación entre los dos elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="dcffb-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="dcffb-108">Se debe usar la función **CreateSortedAddressPairs** en lugar de la **lista de direcciones de SiO \_ \_ \_ ordenar** ioctl en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcffb-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="dcffb-109">En las secciones siguientes se describen las consideraciones de uso para la **\_ \_ \_ ordenación** de la lista de direcciones de SiO.</span><span class="sxs-lookup"><span data-stu-id="dcffb-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="dcffb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcffb-110">Parameters</span></span>

<span data-ttu-id="dcffb-111">El búfer pasado a **la \_ \_ \_ ordenación** de la lista de direcciones de SiO es una estructura de [**\_ \_ lista de direcciones de socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcffb-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="dcffb-112">Cada [**\_ dirección de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) de la lista debe tener el \_ formato SOCKADDR IN6.</span><span class="sxs-lookup"><span data-stu-id="dcffb-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="dcffb-113">La **\_ \_ \_ ordenación** de la lista de direcciones de SiO ordena las direcciones IPv6 e IPv4 en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcffb-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="dcffb-114">Cualquier dirección IPv4 de la lista que se va a ordenar debe estar en el formato de dirección IPv6 asignado a IPv4.</span><span class="sxs-lookup"><span data-stu-id="dcffb-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="dcffb-115">Para obtener más información sobre el formato de dirección IPv6 asignado a IPv4, consulte [sockets de dos pilas](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="dcffb-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="dcffb-116">En Windows Server 2003 y Windows XP, la **\_ \_ \_ ordenación** de la lista de direcciones de SiO solo ordena direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="dcffb-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="dcffb-117">No se admiten las direcciones IPv4 en el formato de dirección IPv6 asignado a IPv4.</span><span class="sxs-lookup"><span data-stu-id="dcffb-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="dcffb-118">En la salida, el miembro **iAddressCount** de la estructura de la [**lista de \_ direcciones \_ de socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) puede ser menor que en la entrada si el código ioctl determina que algunas direcciones de destino no son válidas.</span><span class="sxs-lookup"><span data-stu-id="dcffb-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="dcffb-119">Determinación de ordenación</span><span class="sxs-lookup"><span data-stu-id="dcffb-119">Sorting Determination</span></span>

<span data-ttu-id="dcffb-120">El criterio de ordenación para las direcciones IPv6 para la lista de direcciones de SIO la \_ \_ \_ ordenación ioctl se basa en la tabla de directivas de prefijos.</span><span class="sxs-lookup"><span data-stu-id="dcffb-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="dcffb-121">La tabla de directivas de prefijos se configura mediante la utilidad de línea de comandos *Netsh.exe* .</span><span class="sxs-lookup"><span data-stu-id="dcffb-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="dcffb-122">Los siguientes fragmentos de código de línea de comandos ilustran los comandos de configuración de tabla de directiva de prefijo *Netsh.exe* básica:</span><span class="sxs-lookup"><span data-stu-id="dcffb-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="dcffb-123">En Windows Server 2003 y Windows XP, el primer comando netsh indicado anteriormente era el siguiente.</span><span class="sxs-lookup"><span data-stu-id="dcffb-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="dcffb-124">Todos los demás comandos relacionados son los mismos.</span><span class="sxs-lookup"><span data-stu-id="dcffb-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="dcffb-125">La ordenación de direcciones también viene determinada por un algoritmo descrito en la RFC 3484 en la *selección de direcciones predeterminada para el protocolo de Internet versión 6 (IPv6)* publicado por IETF.</span><span class="sxs-lookup"><span data-stu-id="dcffb-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="dcffb-126">Para más información, consulte [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span><span class="sxs-lookup"><span data-stu-id="dcffb-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="dcffb-127">(Este recurso solo está disponible en inglés).</span><span class="sxs-lookup"><span data-stu-id="dcffb-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="dcffb-128">La **\_ \_ \_ ordenación** de la lista de direcciones de SiO ordena las direcciones de mejor a peor, y rellena los miembros de **\_ \_ identificador de ámbito de sin6** , si es necesario.</span><span class="sxs-lookup"><span data-stu-id="dcffb-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="dcffb-129">En el caso de las direcciones locales del sitio, \_ la ordenación de la lista de direcciones de SiO se \_ \_ rellena en el identificador de ámbito o quita la dirección.</span><span class="sxs-lookup"><span data-stu-id="dcffb-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="dcffb-130">El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO omite la dirección de origen enlazada al socket y solo ordena por la lista de direcciones de destino pasada como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="dcffb-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="dcffb-131">Se debe usar la función [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) en lugar de la **lista de direcciones de SiO \_ \_ \_ ordenar** ioctl en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcffb-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="dcffb-132">La función **CreateSortedAddressPairs** devuelve una lista de pares de direcciones que contiene una dirección de origen local y una dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="dcffb-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="dcffb-133">Esto proporciona a una aplicación la dirección de origen correcta que se va a usar para cada dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="dcffb-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="dcffb-134">Una aplicación también puede filtrar los resultados buscando una dirección de origen concreta.</span><span class="sxs-lookup"><span data-stu-id="dcffb-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="dcffb-135">en los resultados.</span><span class="sxs-lookup"><span data-stu-id="dcffb-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcffb-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcffb-136">Requirements</span></span>

<span data-ttu-id="dcffb-137">El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO se define en el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="dcffb-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="dcffb-138">En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y la **lista de direcciones de dirección de SiO \_ \_ \_** se define ioctl en el archivo de encabezado *Ws2def. h* .</span><span class="sxs-lookup"><span data-stu-id="dcffb-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="dcffb-139">Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="dcffb-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="dcffb-140">El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO es compatible con Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcffb-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcffb-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dcffb-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcffb-142">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="dcffb-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
