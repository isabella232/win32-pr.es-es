---
description: El repositorio WMI contiene clases de rendimiento preinstaladas para todos los objetos de la biblioteca de rendimiento.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Obtener acceso a las clases de rendimiento preinstaladas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697252"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a><span data-ttu-id="c7b1c-103">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="c7b1c-103">Accessing WMI Preinstalled Performance Classes</span></span>

<span data-ttu-id="c7b1c-104">El repositorio WMI contiene clases de rendimiento preinstaladas para todos los objetos de la biblioteca de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-104">The WMI repository contains preinstalled performance classes for all the performance library objects.</span></span> <span data-ttu-id="c7b1c-105">Por ejemplo, las instancias de la clase de rendimiento datos sin procesar de [**Win32 \_ PerfRawData \_ PerfProc \_ proceso**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representan procesos.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-105">For example, instances of the raw data performance class [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represent processes.</span></span> <span data-ttu-id="c7b1c-106">Este objeto de rendimiento es visible en el monitor de sistema como el objeto de proceso.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-106">This performance object is visible in System Monitor as the Process object.</span></span>

<span data-ttu-id="c7b1c-107">La propiedad **PageFaultsPerSec** del [**\_ \_ \_ proceso PerfProc de Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa el contador de rendimiento de errores de página por segundo para el proceso.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-107">The **PageFaultsPerSec** property of [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represents the Page Faults per second performance counter for the process.</span></span> <span data-ttu-id="c7b1c-108">Las [**clases \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen los valores de datos calculados que se muestran en el monitor de sistema (Perfmon.exe).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-108">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data values displayed in System Monitor (Perfmon.exe).</span></span> <span data-ttu-id="c7b1c-109">El valor de la propiedad **PageFaultsPerSec** del [**\_ \_ \_ proceso PerfProc de Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) es el mismo que cuando aparece en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-109">The value of the **PageFaultsPerSec** property of [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) is the same as when it appears in System Monitor.</span></span>

<span data-ttu-id="c7b1c-110">Use la [API de com para WMI](com-api-for-wmi.md) o la [API de scripting para WMI](scripting-api-for-wmi.md) para tener acceso a los datos de rendimiento a través de las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-110">Use either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md) to access performance data through the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="c7b1c-111">En ambos casos, se requiere un objeto de [*actualización*](gloss-r.md) para obtener cada muestra de datos.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-111">In both cases a [*refresher*](gloss-r.md) object is required to obtain each data sample.</span></span> <span data-ttu-id="c7b1c-112">Para obtener más información y ejemplos de código de script para el uso de los actualizadores y el acceso a las clases de rendimiento, vea [tareas de WMI: supervisión del rendimiento](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-112">For more information and script code examples for using refreshers and accessing performance classes, see [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span> <span data-ttu-id="c7b1c-113">Para obtener más información, vea [obtener acceso a los datos de rendimiento en script](accessing-performance-data-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-113">For more information, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md).</span></span>

## <a name="accessing-performance-data-from-c"></a><span data-ttu-id="c7b1c-114">Obtener acceso a los datos de rendimiento de C++</span><span class="sxs-lookup"><span data-stu-id="c7b1c-114">Accessing Performance Data from C++</span></span>

<span data-ttu-id="c7b1c-115">En el siguiente ejemplo de código de C++ se utiliza el proveedor de contador de rendimiento para tener acceso a las clases predefinidas de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-115">The following C++ code example uses the Performance Counter provider to access predefined high-performance classes.</span></span> <span data-ttu-id="c7b1c-116">Crea un objeto actualizador y agrega un objeto al actualizador.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-116">It creates a refresher object and adds an object to the refresher.</span></span> <span data-ttu-id="c7b1c-117">El objeto es una instancia de [**\_ \_ \_ proceso PerfProc de Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) que supervisa el rendimiento de un proceso específico.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-117">The object is a [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instance that monitors the performance of a specific process.</span></span> <span data-ttu-id="c7b1c-118">El código solo Lee una propiedad de contador en el objeto de proceso, la propiedad **VirtualBytes** .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-118">The code only reads one counter property in the process object, the **VirtualBytes** property.</span></span> <span data-ttu-id="c7b1c-119">El código requiere las siguientes referencias y instrucciones **\# include** para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-119">The code requires the following references and **\#include** statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="c7b1c-120">En el procedimiento siguiente se muestra cómo obtener acceso a los datos de un proveedor de alto rendimiento en C++.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-120">The following procedure shows how to access data from a high-performance provider in C++.</span></span>

<span data-ttu-id="c7b1c-121">**Para tener acceso a los datos de un proveedor de alto rendimiento en C++**</span><span class="sxs-lookup"><span data-stu-id="c7b1c-121">**To access data from a high-performance provider in C++**</span></span>

1.  <span data-ttu-id="c7b1c-122">Establezca una conexión con el espacio de nombres WMI y establezca la seguridad de WMI mediante una llamada a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) y [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-122">Establish a connection to the WMI namespace, and set WMI security by using a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) and [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="c7b1c-123">Este paso es un paso estándar para crear cualquier aplicación cliente de WMI.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-123">This step is a standard step for creating any WMI client application.</span></span> <span data-ttu-id="c7b1c-124">Para obtener más información, vea [crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-124">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

2.  <span data-ttu-id="c7b1c-125">Cree un objeto actualizador mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ WbemRefresher.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-125">Create a refresher object by using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_WbemRefresher.</span></span> <span data-ttu-id="c7b1c-126">Solicite una interfaz [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) a través del método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-126">Request an [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) interface through the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="c7b1c-127">Solicite una interfaz [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) a través del método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-127">Request an [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface through the **QueryInterface** method.</span></span>

    <span data-ttu-id="c7b1c-128">La interfaz [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) es la interfaz principal del objeto [**actualizador**](swbemrefreshableitem-refresher.md) de WMI.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-128">The [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface is the main interface for the WMI [**Refresher**](swbemrefreshableitem-refresher.md) object.</span></span>

    <span data-ttu-id="c7b1c-129">En el ejemplo de código de C++ siguiente se muestra cómo recuperar [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-129">The following C++ code example shows how to retrieve [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span></span>

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  <span data-ttu-id="c7b1c-130">Agregue un objeto al actualizador a través de una llamada al método [**IWbemConfigureRefresher:: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-130">Add an object to the refresher through a call to the [**IWbemConfigureRefresher::AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) method.</span></span>

    <span data-ttu-id="c7b1c-131">Cuando se agrega un objeto al actualizador, WMI actualiza el objeto cada vez que se llama al método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-131">When you add an object to the refresher, WMI refreshes the object whenever you call the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method.</span></span> <span data-ttu-id="c7b1c-132">El objeto que agrega designa el proveedor en sus calificadores de clase.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-132">The object you add designates the provider in its class qualifiers.</span></span>

    <span data-ttu-id="c7b1c-133">En el ejemplo de código de C++ siguiente se muestra cómo llamar a [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-133">The following C++ code example shows how to call [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span></span>

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  <span data-ttu-id="c7b1c-134">Para configurar un acceso más rápido al objeto, conéctese a la interfaz [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) a través de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-134">To set up faster access to the object, connect to the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span>

    <span data-ttu-id="c7b1c-135">En el ejemplo de código de C++ siguiente se muestra cómo recuperar un puntero al objeto mediante [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) en lugar de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-135">The following C++ code example shows how to retrieve a pointer to the object using [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instead of [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span></span>

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    <span data-ttu-id="c7b1c-136">La interfaz [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) aumenta el rendimiento porque puede obtener los identificadores de las propiedades de contador específicas y requiere que bloquee y desbloquee el objeto en el código, que es una operación que [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) realiza para cada acceso de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-136">The [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface increases performance because you can get handles to specific counter properties, and it requires that you lock and unlock the object in your code, which is an operation that [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) performs for each property access.</span></span>

5.  <span data-ttu-id="c7b1c-137">Obtenga los identificadores de las propiedades que se van a examinar mediante llamadas al método [**IWbemObjectAccess:: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-137">Obtain the handles of the properties to examine by using calls to the [**IWbemObjectAccess::GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

    <span data-ttu-id="c7b1c-138">Los identificadores de propiedad son los mismos para todas las instancias de una clase, lo que significa que usan el identificador de propiedad que se recupera de una instancia específica para todas las instancias de una clase específica.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-138">Property handles are the same for all instances of a class, which means that use the property handle you retrieve from a specific instance for all instances of a specific class.</span></span> <span data-ttu-id="c7b1c-139">También puede obtener un identificador de un objeto de clase para recuperar los valores de propiedad de un objeto de instancia.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-139">You can also obtain a handle from a class object to retrieve property values from an instance object.</span></span>

    <span data-ttu-id="c7b1c-140">En el ejemplo de código de C++ siguiente se muestra cómo recuperar un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-140">The following C++ code example shows how to retrieve a property handle.</span></span>

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  <span data-ttu-id="c7b1c-141">Cree un bucle de programación que realice las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="c7b1c-141">Create a programming loop that performs the following actions:</span></span>

    -   <span data-ttu-id="c7b1c-142">Actualice el objeto con una llamada a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) mediante el puntero creado en la llamada anterior a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c7b1c-142">Refresh the object with a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) by using the pointer created in the previous call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

        <span data-ttu-id="c7b1c-143">En esta llamada, el actualizador de WMI actualiza el objeto de cliente con los datos proporcionados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-143">In this call, the WMI Refresher refreshes the client object by using data that the provider supplies.</span></span>

    -   <span data-ttu-id="c7b1c-144">Realice cualquier acción según sea necesario en el objeto, como la recuperación de un nombre de propiedad, un tipo de datos o un valor.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-144">Perform any action as necessary on the object, such as retrieving a property name, data type, or value.</span></span>

        <span data-ttu-id="c7b1c-145">Puede tener acceso a la propiedad mediante el identificador de propiedad obtenido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-145">You can access the property through the property handle obtained earlier.</span></span> <span data-ttu-id="c7b1c-146">Debido a la llamada de [**actualización**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , WMI actualiza la propiedad cada vez a través del bucle.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-146">Due to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) call, WMI refreshes the property each time through the loop.</span></span>

<span data-ttu-id="c7b1c-147">En el siguiente ejemplo de C++ se muestra cómo usar la API de alto rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-147">The following C++ example shows how to use the WMI high-performance API.</span></span>


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a><span data-ttu-id="c7b1c-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7b1c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b1c-149">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="c7b1c-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="c7b1c-150">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="c7b1c-150">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
