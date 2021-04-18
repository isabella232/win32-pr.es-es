---
title: Administrar direcciones IP con AddIPAddress, DeleteIPAddress
description: La función AddIPAddress agrega la dirección IPv4 especificada al adaptador especificado.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687452"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="896c2-103">Administrar direcciones IP con AddIPAddress, DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="896c2-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="896c2-104">La función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) agrega la dirección IPv4 especificada al adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="896c2-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="896c2-105">La función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) elimina la dirección IPv4 especificada del adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="896c2-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="896c2-106">Estas funciones se pueden usar para agregar y eliminar direcciones IPv4 a un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="896c2-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="896c2-107">Una dirección IPv4 agregada por la función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) no es persistente.</span><span class="sxs-lookup"><span data-stu-id="896c2-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="896c2-108">La dirección IPv4 solo existe mientras exista el objeto de adaptador.</span><span class="sxs-lookup"><span data-stu-id="896c2-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="896c2-109">Al reiniciar el equipo, se destruye la dirección IPv4, al igual que se restablece manualmente la tarjeta de interfaz de red (NIC).</span><span class="sxs-lookup"><span data-stu-id="896c2-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="896c2-110">Después de llamar a [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) correctamente, se deshabilitará DHCP para la dirección IP que se agregó.</span><span class="sxs-lookup"><span data-stu-id="896c2-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="896c2-111">Por lo tanto, las funciones como [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), que requieren que se habilite DHCP, no funcionarán en la dirección IP agregada.</span><span class="sxs-lookup"><span data-stu-id="896c2-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="896c2-112">La función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) se puede usar para eliminar la dirección IPv4 agregada.</span><span class="sxs-lookup"><span data-stu-id="896c2-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="896c2-113">Las directivas de grupo, las directivas de empresa y otras restricciones de la red pueden impedir que estas funciones se completen correctamente.</span><span class="sxs-lookup"><span data-stu-id="896c2-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="896c2-114">Asegúrese de que la aplicación tiene los permisos de red necesarios antes de intentar usar estas funciones.</span><span class="sxs-lookup"><span data-stu-id="896c2-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="896c2-115">**Para usar AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="896c2-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="896c2-116">Declare las variables **ULong** denominadas `NTEContext` y `NTEInstance` , inicializadas en cero.</span><span class="sxs-lookup"><span data-stu-id="896c2-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="896c2-117">La `NTEContext` variable es el único parámetro de la función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) ; para eliminar la dirección IP que se agrega, `NTEContext` se debe almacenar y sin modificar.</span><span class="sxs-lookup"><span data-stu-id="896c2-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="896c2-118">Declare las variables para las estructuras DirIP y IPMask denominadas `iaIPAddress` y `iaIPMask` , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="896c2-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="896c2-119">Estos valores son simplemente enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="896c2-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="896c2-120">Inicialice las `iaIPAddress` `iaIPMask` variables y con la función de [**\_ Dirección inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .</span><span class="sxs-lookup"><span data-stu-id="896c2-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="896c2-121">Llame a la función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para agregar la dirección IPv4.</span><span class="sxs-lookup"><span data-stu-id="896c2-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="896c2-122">Compruebe si hay errores y devuelva el valor de error a la variable **DWORD** `dwRetVal` (para una comprobación de errores más extensa).</span><span class="sxs-lookup"><span data-stu-id="896c2-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="896c2-123">El tercer parámetro es el índice del adaptador, que se puede obtener mediante una llamada a la función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="896c2-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="896c2-124">Se supone que la variable devuelta por esta función se denomina `pIPAddrTable` .</span><span class="sxs-lookup"><span data-stu-id="896c2-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="896c2-125">Para obtener ayuda con la función **GetIpAddrTable** , consulte [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="896c2-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="896c2-126">**Para usar DeleteIpAddress**</span><span class="sxs-lookup"><span data-stu-id="896c2-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="896c2-127">Llame a la función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , pasando la `NTEContext` variable como su parámetro.</span><span class="sxs-lookup"><span data-stu-id="896c2-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="896c2-128">Compruebe si hay errores y devuelva el valor de error a la variable **DWORD** `dwRetVal` (para una comprobación de errores más extensa).</span><span class="sxs-lookup"><span data-stu-id="896c2-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="896c2-129">Para usar [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), primero se debe llamar a [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para obtener el identificador `NTEContext` .</span><span class="sxs-lookup"><span data-stu-id="896c2-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="896c2-130">En el procedimiento anterior se supone que ya se ha llamado a **AddIPAddress** en algún lugar del código y que se ha `NTEContext` guardado y permanece sin dañar.</span><span class="sxs-lookup"><span data-stu-id="896c2-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="896c2-131">Siguiente paso: [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="896c2-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="896c2-132">Paso anterior: [Administración de concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="896c2-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
