---
description: La API de alto rendimiento de WMI es una serie de interfaces que obtienen datos de las clases de contador de rendimiento.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Obtener acceso a los datos de rendimiento en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697847"
---
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="a8f58-103">Obtener acceso a los datos de rendimiento en C++</span><span class="sxs-lookup"><span data-stu-id="a8f58-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="a8f58-104">La API de alto rendimiento de WMI es una serie de interfaces que obtienen datos de [las clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="a8f58-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="a8f58-105">Estas interfaces requieren el uso de un objeto [*actualizador*](gloss-r.md) para aumentar la velocidad de muestreo.</span><span class="sxs-lookup"><span data-stu-id="a8f58-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="a8f58-106">Para obtener más información sobre cómo usar el objeto actualizador en scripting, vea [obtener acceso a los datos de rendimiento en scripts](accessing-performance-data-in-script.md) y [tareas WMI: supervisión del rendimiento](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="a8f58-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="a8f58-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="a8f58-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="a8f58-108">Actualizar los datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8f58-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="a8f58-109">Agregar enumeradores al actualizador de WMI</span><span class="sxs-lookup"><span data-stu-id="a8f58-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="a8f58-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8f58-110">Example</span></span>](#example)
-   [<span data-ttu-id="a8f58-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8f58-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="a8f58-112">Actualizar los datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8f58-112">Refreshing Performance Data</span></span>

<span data-ttu-id="a8f58-113">Un objeto de actualización aumenta el rendimiento del cliente y del proveedor de datos mediante la recuperación de datos sin cruzar los límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="a8f58-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="a8f58-114">Si el cliente y el servidor se encuentran en el mismo equipo, un actualizador carga el proveedor de alto rendimiento en proceso en el cliente y copia los datos directamente de los objetos de proveedor en objetos de cliente.</span><span class="sxs-lookup"><span data-stu-id="a8f58-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="a8f58-115">Si el cliente y el servidor se encuentran en equipos diferentes, el actualizador aumenta el rendimiento mediante el almacenamiento en caché de objetos en el equipo remoto y la transmisión de los conjuntos de datos mínimos al cliente.</span><span class="sxs-lookup"><span data-stu-id="a8f58-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="a8f58-116">Un actualizador también:</span><span class="sxs-lookup"><span data-stu-id="a8f58-116">A refresher also:</span></span>

-   <span data-ttu-id="a8f58-117">Vuelve a conectar automáticamente un cliente a un servicio WMI remoto cuando se produce un error de red o cuando se reinicia el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="a8f58-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="a8f58-118">De forma predeterminada, un actualizador intenta volver a conectar la aplicación al proveedor de alto rendimiento pertinente cuando se produce un error en una conexión remota entre los dos equipos.</span><span class="sxs-lookup"><span data-stu-id="a8f58-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="a8f58-119">Para evitar la reconexión, pase el **marcador \_ WBEM \_ \_ no actualizar \_ \_** la marca de reconexión automática en la llamada al método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="a8f58-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="a8f58-120">Los clientes de scripting deben establecer la propiedad [**SWbemRefresher. reconexión automática**](swbemrefresher-autoreconnect.md) en **false**.</span><span class="sxs-lookup"><span data-stu-id="a8f58-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="a8f58-121">Carga varios objetos y enumeradores que se proporcionan en el mismo proveedor o en otros diferentes.</span><span class="sxs-lookup"><span data-stu-id="a8f58-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="a8f58-122">Permite agregar varios objetos, enumeradores o ambos a un actualizador.</span><span class="sxs-lookup"><span data-stu-id="a8f58-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="a8f58-123">Enumera los objetos.</span><span class="sxs-lookup"><span data-stu-id="a8f58-123">Enumerates objects.</span></span>

    <span data-ttu-id="a8f58-124">Al igual que otros proveedores, un proveedor de alto rendimiento puede enumerar objetos.</span><span class="sxs-lookup"><span data-stu-id="a8f58-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="a8f58-125">Una vez que termine de escribir el cliente de alto rendimiento, es posible que desee mejorar el tiempo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8f58-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="a8f58-126">Dado que la interfaz [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) está optimizada para la velocidad, la interfaz no se threadsafe de forma intrínseca.</span><span class="sxs-lookup"><span data-stu-id="a8f58-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="a8f58-127">Por lo tanto, durante una operación de actualización, no tiene acceso al objeto actualizable o a la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a8f58-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="a8f58-128">Para proteger los objetos en todos los subprocesos durante las llamadas al método **IWbemObjectAccess** , use los métodos [**IWbemObjectAccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) y [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) .</span><span class="sxs-lookup"><span data-stu-id="a8f58-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="a8f58-129">Para mejorar el rendimiento, sincronice los subprocesos para que no tenga que bloquear los subprocesos individuales.</span><span class="sxs-lookup"><span data-stu-id="a8f58-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="a8f58-130">La reducción de subprocesos y la sincronización de grupos de objetos para las operaciones de actualización proporciona el mejor rendimiento general.</span><span class="sxs-lookup"><span data-stu-id="a8f58-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="a8f58-131">Agregar enumeradores al actualizador de WMI</span><span class="sxs-lookup"><span data-stu-id="a8f58-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="a8f58-132">Tanto el número de instancias como los datos de cada instancia se actualizan agregando un enumerador al actualizador para que cada llamada a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) dé como resultado una enumeración completa.</span><span class="sxs-lookup"><span data-stu-id="a8f58-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="a8f58-133">El siguiente ejemplo de código de C++ requiere las siguientes referencias y \# instrucciones include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8f58-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="a8f58-134">En el procedimiento siguiente se muestra cómo agregar un enumerador a un actualizador.</span><span class="sxs-lookup"><span data-stu-id="a8f58-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="a8f58-135">**Para agregar un enumerador a un actualizador**</span><span class="sxs-lookup"><span data-stu-id="a8f58-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="a8f58-136">Llame al método [**IWbemConfigureRefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) con la ruta de acceso al objeto actualizable y la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="a8f58-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="a8f58-137">El actualizador devuelve un puntero a una interfaz [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) .</span><span class="sxs-lookup"><span data-stu-id="a8f58-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="a8f58-138">Puede usar la interfaz **IWbemHiPerfEnum** para tener acceso a los objetos de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a8f58-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  <span data-ttu-id="a8f58-139">Cree un bucle que realice las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a8f58-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="a8f58-140">Actualiza el objeto mediante una llamada a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span><span class="sxs-lookup"><span data-stu-id="a8f58-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="a8f58-141">Proporciona una matriz de punteros de interfaz [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) al método [**IWbemHiPerfEnum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .</span><span class="sxs-lookup"><span data-stu-id="a8f58-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="a8f58-142">Obtiene acceso a las propiedades del enumerador mediante los métodos [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) pasados a [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="a8f58-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="a8f58-143">Se puede pasar un identificador de propiedad a cada instancia de [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) para recuperar el valor actualizado.</span><span class="sxs-lookup"><span data-stu-id="a8f58-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="a8f58-144">El cliente debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar los punteros **IWbemObjectAccess** devueltos por [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="a8f58-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="a8f58-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8f58-145">Example</span></span>

<span data-ttu-id="a8f58-146">En el siguiente ejemplo de código de C++ se enumera una clase de alto rendimiento, en la que el cliente recupera un identificador de propiedad del primer objeto y reutiliza el identificador para el resto de la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="a8f58-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="a8f58-147">Cada llamada al método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) actualiza el número de instancias y los datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="a8f58-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="a8f58-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8f58-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8f58-149">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8f58-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="a8f58-150">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="a8f58-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="a8f58-151">Actualizar datos WMI en scripts</span><span class="sxs-lookup"><span data-stu-id="a8f58-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="a8f58-152">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8f58-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="a8f58-153">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8f58-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="a8f58-154">Calificadores de propiedad para las clases de contador de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="a8f58-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="a8f58-155">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="a8f58-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="a8f58-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="a8f58-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="a8f58-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="a8f58-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
