---
title: Administrar concesiones DHCP con IpReleaseAddress, IpRenewAddress
description: Las funciones IpReleaseAddress y IpRenewAddress se usan para liberar y renovar la concesión actual del Protocolo de configuración dinámica de host (DHCP).
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907885"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="80a20-103">Administrar concesiones DHCP con IpReleaseAddress, IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="80a20-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="80a20-104">Las funciones [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) se usan para liberar y renovar la concesión actual del Protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="80a20-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="80a20-105">La función **IpReleaseAddress** libera una dirección IPv4 obtenida previamente a través de DHCP.</span><span class="sxs-lookup"><span data-stu-id="80a20-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="80a20-106">La función **IpRenewAddress** renueva una concesión en una dirección IPv4 obtenida previamente a través de DHCP.</span><span class="sxs-lookup"><span data-stu-id="80a20-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="80a20-107">Es habitual utilizar estas dos funciones juntas, primero liberar la concesión con una llamada a **IpReleaseAddress** y, a continuación, renovar la concesión con una llamada a la función **IpRenewAddress** .</span><span class="sxs-lookup"><span data-stu-id="80a20-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="80a20-108">Cuando un cliente DHCP ha obtenido previamente una concesión DHCP y no se llama a [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) antes de la función [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , la solicitud del cliente DHCP se envía al servidor DHCP que emitió la concesión DHCP inicial.</span><span class="sxs-lookup"><span data-stu-id="80a20-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="80a20-109">Es posible que este servidor DHCP no esté disponible o que se produzca un error en la solicitud DHCP.</span><span class="sxs-lookup"><span data-stu-id="80a20-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="80a20-110">Cuando un host ha obtenido previamente una concesión DHCP y se llama a **IpReleaseAddress** antes de la función **IpRenewAddress** , el cliente DHCP libera primero la dirección IP obtenida y envía una solicitud de cliente DHCP para obtener una respuesta de cualquier servidor DHCP disponible.</span><span class="sxs-lookup"><span data-stu-id="80a20-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="80a20-111">Las funciones [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y [**IPRENEWADDRESS**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requieren que DHCP esté habilitado para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="80a20-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="80a20-112">La función [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) toma un puntero a una estructura de mapa de índice del adaptador de [**IP \_ \_ \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) como su único parámetro.</span><span class="sxs-lookup"><span data-stu-id="80a20-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="80a20-113">Para obtener este parámetro, llame primero a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span><span class="sxs-lookup"><span data-stu-id="80a20-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="80a20-114">Para obtener ayuda con la función **GetInterfaceInfo** , consulte [Administración de interfaces con GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="80a20-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="80a20-115">**Para usar IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="80a20-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="80a20-116">Obtener un puntero a una estructura de mapa de índice del adaptador de IP mediante la función [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . [**\_ \_ \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)</span><span class="sxs-lookup"><span data-stu-id="80a20-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="80a20-117">(Para obtener ayuda con la función GetInterfaceInfo, consulte [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="80a20-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="80a20-118">Cree un  objeto DWORD `dwRetVal` (se usa para la comprobación de errores).</span><span class="sxs-lookup"><span data-stu-id="80a20-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="80a20-119">Se supone que se llama a la variable devuelta por **GetInterfaceInfo** `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="80a20-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="80a20-120">Si DHCP está habilitado, llame a la función [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , pasando la variable de [**asignación de índice del \_ adaptador \_ \_ de IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` como su parámetro.</span><span class="sxs-lookup"><span data-stu-id="80a20-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="80a20-121">Compruebe si hay errores generales y devuelva su valor a la variable **DWORD** `dwRetVal` (para una comprobación de errores más extensa).</span><span class="sxs-lookup"><span data-stu-id="80a20-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="80a20-122">La función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) devuelve un parámetro que se puede utilizar para comprobar si DHCP está habilitado antes de llamar a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="80a20-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="80a20-123">Para obtener ayuda con **GetAdaptersInfo**, consulte [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="80a20-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="80a20-124">Es habitual usar estas dos funciones juntas, llamar a la función [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y, a continuación, llamar a la función [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , pasando la misma estructura que el parámetro a ambas funciones.</span><span class="sxs-lookup"><span data-stu-id="80a20-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="80a20-125">En el procedimiento siguiente se supone que las funciones no se usan juntas; sin embargo, si las funciones se usan juntas, omita el paso 1.</span><span class="sxs-lookup"><span data-stu-id="80a20-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="80a20-126">**Para usar IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="80a20-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="80a20-127">Obtener un puntero a una estructura de mapa de índice del adaptador de IP mediante la función [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . [**\_ \_ \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)</span><span class="sxs-lookup"><span data-stu-id="80a20-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="80a20-128">(Para obtener ayuda con la función **GetInterfaceInfo** , consulte [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="80a20-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="80a20-129">Declare un objeto **DWORD** `dwRetVal` (usado para la comprobación de errores) si esta variable no se ha declarado.</span><span class="sxs-lookup"><span data-stu-id="80a20-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="80a20-130">Se supone que se llama a la variable devuelta por **GetInterfaceInfo** `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="80a20-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="80a20-131">Llame a la función [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , pasando la variable de [**asignación de índice del \_ adaptador \_ \_ de IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` como su parámetro.</span><span class="sxs-lookup"><span data-stu-id="80a20-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="80a20-132">Compruebe si hay errores generales y devuelva su valor a la variable **DWORD** `dwRetVal` (para una comprobación de errores más extensa).</span><span class="sxs-lookup"><span data-stu-id="80a20-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="80a20-133">Paso siguiente: [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="80a20-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="80a20-134">Paso anterior: [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="80a20-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



