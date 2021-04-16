---
description: La función GetInterfaceInfo rellena un puntero a una estructura de \_ información de interfaz IP \_ con información sobre las interfaces asociadas al sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Administrar interfaces mediante GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686709"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="74756-103">Administrar interfaces mediante GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="74756-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="74756-104">La función [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) rellena un puntero a una estructura [**de \_ \_ información de interfaz IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) con información sobre las interfaces asociadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="74756-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="74756-105">**Para usar GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="74756-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="74756-106">Declare un puntero a un objeto de [**\_ \_ información de interfaz IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) denominado `pInfo` y un objeto **ULong** denominado `ulOutBufLen` .</span><span class="sxs-lookup"><span data-stu-id="74756-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="74756-107">Declare también un objeto **DWORD** denominado `dwRetVal` (usado para la comprobación de errores).</span><span class="sxs-lookup"><span data-stu-id="74756-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="74756-108">Asigne memoria para las estructuras.</span><span class="sxs-lookup"><span data-stu-id="74756-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="74756-109">El tamaño de `ulOutBufLen` no es suficiente para contener la información.</span><span class="sxs-lookup"><span data-stu-id="74756-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="74756-110">Vea el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="74756-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="74756-111">Realice una llamada inicial a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) para obtener el tamaño necesario en la `ulOutBufLen` variable.</span><span class="sxs-lookup"><span data-stu-id="74756-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="74756-112">Esta llamada a la función está pensada para producir un error y se utiliza para asegurarse de que la `ulOutBufLen` variable especifica un tamaño suficiente para contener toda la información devuelta a `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="74756-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="74756-113">Se trata de un modelo de programación común en la aplicación auxiliar de IP para las estructuras de datos y las funciones de este tipo.</span><span class="sxs-lookup"><span data-stu-id="74756-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="74756-114">Realice una segunda llamada a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) con la comprobación de errores general y devuelva su valor a la variable **DWORD** `dwRetVal` (para la comprobación de errores más avanzada).</span><span class="sxs-lookup"><span data-stu-id="74756-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="74756-115">Si la llamada se realizó correctamente, acceda a los datos de la `pInfo` estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="74756-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="74756-116">% WS en la primera línea denota una cadena de tipo ancho.</span><span class="sxs-lookup"><span data-stu-id="74756-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="74756-117">Se utiliza porque el atributo **Name** de la estructura [**de \_ \_ \_ asignación de índice del adaptador de IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` es **WCHAR**, que es una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="74756-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="74756-118">Libere cualquier memoria asignada para la estructura *Pinfo* .</span><span class="sxs-lookup"><span data-stu-id="74756-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="74756-119">Siguiente paso: [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="74756-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="74756-120">Paso anterior: [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="74756-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



