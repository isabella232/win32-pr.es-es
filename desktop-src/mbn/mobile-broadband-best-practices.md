---
description: Al trabajar con la API de banda ancha móvil, se debe usar el siguiente conjunto de prácticas recomendadas para lograr el mejor rendimiento posible.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Procedimientos recomendados de API de banda ancha móvil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275507"
---
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="57513-103">Procedimientos recomendados de API de banda ancha móvil</span><span class="sxs-lookup"><span data-stu-id="57513-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="57513-104">Al trabajar con la API de banda ancha móvil, se debe usar el siguiente conjunto de prácticas recomendadas para lograr el mejor rendimiento posible.</span><span class="sxs-lookup"><span data-stu-id="57513-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="57513-105">No almacenar en caché objetos funcionales</span><span class="sxs-lookup"><span data-stu-id="57513-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="57513-106">Los objetos funcionales, como [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) y otros, se obtienen de los objetos de administrador, como [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), mediante el método de enumeración en el objeto de administrador correspondiente.</span><span class="sxs-lookup"><span data-stu-id="57513-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="57513-107">No almacene en caché estos objetos funcionales, ya que los objetos funcionales almacenados en caché contienen datos obsoletos.</span><span class="sxs-lookup"><span data-stu-id="57513-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="57513-108">Las operaciones sincrónicas realizadas en estos objetos funcionales devolverán los mismos datos hasta que se obtengan de nuevo los objetos funcionales.</span><span class="sxs-lookup"><span data-stu-id="57513-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="57513-109">En su lugar, almacene en caché los objetos de administrador y obtenga los objetos funcionales del objeto de administrador mediante el método de enumeración en el objeto de administrador correspondiente de nuevo para obtener los datos más recientes.</span><span class="sxs-lookup"><span data-stu-id="57513-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="57513-110">En el ejemplo de código siguiente se muestra la manera adecuada de almacenar en memoria caché los objetos de administrador.</span><span class="sxs-lookup"><span data-stu-id="57513-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a><span data-ttu-id="57513-111">Control de todas las notificaciones</span><span class="sxs-lookup"><span data-stu-id="57513-111">Handle All Notifications</span></span>

<span data-ttu-id="57513-112">Siga y controle todas las notificaciones, incluso si la aplicación no la desencadena.</span><span class="sxs-lookup"><span data-stu-id="57513-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="57513-113">Esto es necesario para mantener la interfaz de usuario sincronizada con el estado real del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57513-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="57513-114">Puede haber más de un administrador de conexiones que se ejecute en un equipo.</span><span class="sxs-lookup"><span data-stu-id="57513-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="57513-115">La interfaz de usuario de la interfaz de red disponible de vista nativa proporcionada por Windows 7 es un administrador de conexiones.</span><span class="sxs-lookup"><span data-stu-id="57513-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="57513-116">Cualquier otro administrador de conexiones debe responder a todas las notificaciones para permanecer sincronizando la interfaz de usuario nativa de Windows.</span><span class="sxs-lookup"><span data-stu-id="57513-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="57513-117">Un usuario puede optar por realizar alguna operación en uno de los administradores de conexiones, lo que puede dar lugar a un cambio de estado del dispositivo de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="57513-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="57513-118">Sin embargo, otros administradores de conexiones deben permanecer actualizados para indicar correctamente el estado modificado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57513-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="57513-119">Por ejemplo, si realiza una conexión mediante uno de los administradores de conexiones, cambiará el estado del dispositivo de disponible a conectado.</span><span class="sxs-lookup"><span data-stu-id="57513-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="57513-120">Este cambio debe estar visible para los administradores de conexión que no iniciaron esta acción.</span><span class="sxs-lookup"><span data-stu-id="57513-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="57513-121">Todos los administradores de conexión que tienen una interfaz de usuario que indica el estado de conexión del dispositivo, deben escuchar y controlar las notificaciones de estado de conexión para actualizar correctamente su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="57513-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="57513-122">Envío y recepción de bytes</span><span class="sxs-lookup"><span data-stu-id="57513-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="57513-123">Use las funciones auxiliares de IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) y [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) para enviar y recibir bytes.</span><span class="sxs-lookup"><span data-stu-id="57513-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="57513-124">Uso de la API de PIN desbloqueado</span><span class="sxs-lookup"><span data-stu-id="57513-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="57513-125">Una aplicación cliente de llamada debe elevarse para poder invocar correctamente [**IMbnPin:: unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span><span class="sxs-lookup"><span data-stu-id="57513-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="57513-126">Este método es la única parte de la API de banda ancha móvil que requiere privilegios de administrador o NCO.</span><span class="sxs-lookup"><span data-stu-id="57513-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="57513-127">Para obtener más información, vea [una descripción del grupo operadores de configuración de red]( https://support.microsoft.com/kb/297938/en-us) .</span><span class="sxs-lookup"><span data-stu-id="57513-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="57513-128">Trabajar con SafeArray</span><span class="sxs-lookup"><span data-stu-id="57513-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="57513-129">Use ZeroMemory () antes de tener acceso a los elementos de un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="57513-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="57513-130">No Compruebe los índices de una SafeArray.</span><span class="sxs-lookup"><span data-stu-id="57513-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="57513-131">Pueden ser negativos.</span><span class="sxs-lookup"><span data-stu-id="57513-131">They may be negative.</span></span>

<span data-ttu-id="57513-132">En el ejemplo de código siguiente se muestra cómo administrar correctamente una SafeArray.</span><span class="sxs-lookup"><span data-stu-id="57513-132">The following code example shows how to properly handle a SafeArray.</span></span>


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
