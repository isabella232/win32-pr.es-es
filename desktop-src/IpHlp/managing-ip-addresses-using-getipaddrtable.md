---
description: La función GetIpAddrTable rellena un puntero a una estructura MIB \_ IPADDRTABLE con información sobre las direcciones IP actuales asociadas al sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Administración de direcciones IP mediante GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909493"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="f7c47-103">Administración de direcciones IP mediante GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="f7c47-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="f7c47-104">La función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) rellena un puntero a una estructura [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) con información sobre las direcciones IP actuales asociadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="f7c47-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="f7c47-105">**Para usar GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="f7c47-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="f7c47-106">Declare un puntero a un objeto [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) denominado *PIPAddrTable* y un objeto **DWORD** denominado *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="f7c47-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="f7c47-107">Estas variables se pasan como parámetros a la función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="f7c47-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="f7c47-108">Cree también una variable **DWORD** denominada *dwRetVal* (que se usa para la comprobación de errores).</span><span class="sxs-lookup"><span data-stu-id="f7c47-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="f7c47-109">Asigne memoria para la estructura.</span><span class="sxs-lookup"><span data-stu-id="f7c47-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="f7c47-110">El tamaño de *dwSize* no es suficiente para contener la información.</span><span class="sxs-lookup"><span data-stu-id="f7c47-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="f7c47-111">Vea el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="f7c47-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="f7c47-112">Realice una llamada inicial a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) para obtener el tamaño necesario en la variable *dwSize* .</span><span class="sxs-lookup"><span data-stu-id="f7c47-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="f7c47-113">Esta llamada a la función está pensada para producir un error y se utiliza para asegurarse de que la variable *dwSize* especifica un tamaño suficiente para contener toda la información devuelta a *pIPAddrTable*.</span><span class="sxs-lookup"><span data-stu-id="f7c47-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="f7c47-114">Se trata de un modelo de programación común para las estructuras de datos y las funciones de este tipo.</span><span class="sxs-lookup"><span data-stu-id="f7c47-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="f7c47-115">Realice una segunda llamada a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) con la comprobación de errores general y devuelva su valor a la variable **DWORD** *dwRetVal* (para la comprobación de errores más avanzada).</span><span class="sxs-lookup"><span data-stu-id="f7c47-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="f7c47-116">Si la llamada se realizó correctamente, acceda a los datos de la estructura de datos *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="f7c47-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="f7c47-117">Libere cualquier memoria asignada para la estructura *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="f7c47-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="f7c47-118">Los  objetos DWORD *dwAddr* y *dwMask* se devuelven como valores numéricos en el orden de bytes del host, no en el orden de bytes de red.</span><span class="sxs-lookup"><span data-stu-id="f7c47-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="f7c47-119">Estos valores no son direcciones IP con puntos.</span><span class="sxs-lookup"><span data-stu-id="f7c47-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="f7c47-120">Paso siguiente: [Administración de concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="f7c47-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="f7c47-121">Paso anterior: [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f7c47-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
