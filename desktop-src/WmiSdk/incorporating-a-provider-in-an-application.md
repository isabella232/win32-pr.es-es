---
description: Describe cómo incluir el proveedor COM de WMI como componente dentro de una aplicación en lugar de en el proceso de WMI. Denominado proveedor desacoplado, este es el tipo recomendado de proveedor COM de WMI que se va a crear para los sistemas operativos Windows 2000 y versiones posteriores.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Incorporación de un proveedor en una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104549909"
---
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="5693a-104">Incorporación de un proveedor en una aplicación</span><span class="sxs-lookup"><span data-stu-id="5693a-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="5693a-105">Al crear una aplicación que se va a instrumentar, el procedimiento recomendado consiste en incluir el proveedor como un componente dentro de la propia aplicación.</span><span class="sxs-lookup"><span data-stu-id="5693a-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="5693a-106">Esta práctica permite que Instrumental de administración de Windows (WMI) interactúe directamente con el proveedor de servicios en lugar de hacerlo indirectamente a través de la API de programa.</span><span class="sxs-lookup"><span data-stu-id="5693a-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="5693a-107">Desacoplar el proveedor de WMI también pone a la aplicación en el control de la duración del proveedor, en lugar de WMI.</span><span class="sxs-lookup"><span data-stu-id="5693a-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="5693a-108">Para obtener más información sobre cómo escribir un proveedor que se ejecuta en el proceso WMI, vea [proporcionar datos a WMI escribiendo un proveedor](supplying-data-to-wmi-by-writing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5693a-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="5693a-109">Para obtener más información sobre el modelo de hospedaje y la configuración de seguridad para el proveedor, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="5693a-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="5693a-110">En el diagrama siguiente se ilustra la relación entre WMI, un proveedor desacoplado y una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5693a-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![relación entre WMI, el proveedor desacoplado y la aplicación](images/decoupledprov.png)

<span data-ttu-id="5693a-112">Para obtener más información sobre los métodos de proveedor desacoplados, vea [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) y [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span><span class="sxs-lookup"><span data-stu-id="5693a-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="5693a-113">El proveedor desacoplado admite la instancia, el método, los proveedores de eventos y los consumidores de eventos.</span><span class="sxs-lookup"><span data-stu-id="5693a-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="5693a-114">No admite proveedores de clases y propiedades.</span><span class="sxs-lookup"><span data-stu-id="5693a-114">It does not support class and property providers.</span></span> <span data-ttu-id="5693a-115">Para obtener más información, consulte [escribir un proveedor de clases](writing-a-class-provider.md) y [escribir un proveedor de propiedades](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5693a-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="5693a-116">Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="5693a-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="5693a-117">En el procedimiento siguiente se usan ejemplos de código de C++ para describir cómo incorporar un proveedor desacoplado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5693a-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="5693a-118">El método de inicialización de la aplicación realiza los pasos siguientes para que WMI solo interactúe con un proveedor desacoplado registrado.</span><span class="sxs-lookup"><span data-stu-id="5693a-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="5693a-119">**Para implementar un proveedor desacoplado en una aplicación de C++**</span><span class="sxs-lookup"><span data-stu-id="5693a-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="5693a-120">Inicializa la biblioteca COM para que la use el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="5693a-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="5693a-121">En el ejemplo de código siguiente se muestra cómo inicializar la biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="5693a-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="5693a-122">Establezca el nivel de seguridad de proceso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5693a-122">Set the default process security level.</span></span>

    <span data-ttu-id="5693a-123">Este nivel establece el nivel de seguridad necesario para que otros procesos tengan acceso a la información del proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="5693a-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="5693a-124">El nivel de autenticación debe ser el nivel predeterminado de autenticación de RPC \_ C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5693a-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="5693a-125">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="5693a-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="5693a-126">En el ejemplo de código siguiente se muestra cómo establecer el nivel de seguridad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5693a-126">The following code example shows how to set the default security level.</span></span>

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  <span data-ttu-id="5693a-127">Registra el registrador de proveedores desacoplado.</span><span class="sxs-lookup"><span data-stu-id="5693a-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="5693a-128">En el ejemplo de código siguiente se muestra cómo registrar el registrador de proveedores desacoplado.</span><span class="sxs-lookup"><span data-stu-id="5693a-128">The following code example shows how to register the decoupled provider registrar.</span></span>

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  <span data-ttu-id="5693a-129">Registre el proveedor de eventos desacoplado.</span><span class="sxs-lookup"><span data-stu-id="5693a-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="5693a-130">En el ejemplo de código siguiente se muestra cómo registrar el proveedor de eventos desacoplado.</span><span class="sxs-lookup"><span data-stu-id="5693a-130">The following code example shows how to register the decoupled event provider.</span></span>

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  <span data-ttu-id="5693a-131">Realice las [llamadas a WMI](making-calls-to-wmi.md) requeridas por la funcionalidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5693a-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="5693a-132">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="5693a-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="5693a-133">Para obtener más información si el proveedor presta servicio a una solicitud de datos de un script o una aplicación, consulte [Suplantar a un cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="5693a-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="5693a-134">Justo antes de finalizar, la aplicación debe limpiarse después.</span><span class="sxs-lookup"><span data-stu-id="5693a-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="5693a-135">En el procedimiento siguiente se describe cómo anular el registro del proveedor desacoplado para que WMI no intente consultarlo para obtener información.</span><span class="sxs-lookup"><span data-stu-id="5693a-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="5693a-136">En el procedimiento siguiente se describe cómo anular el registro del proveedor desacoplado.</span><span class="sxs-lookup"><span data-stu-id="5693a-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="5693a-137">**Para anular el registro del proveedor desacoplado**</span><span class="sxs-lookup"><span data-stu-id="5693a-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="5693a-138">Anular el registro y liberar el registrador.</span><span class="sxs-lookup"><span data-stu-id="5693a-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="5693a-139">En el ejemplo de código siguiente se muestra cómo anular el registro y liberar el registrador.</span><span class="sxs-lookup"><span data-stu-id="5693a-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="5693a-140">Anule el registro del proveedor de eventos y suéltelo.</span><span class="sxs-lookup"><span data-stu-id="5693a-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="5693a-141">En el ejemplo de código siguiente se muestra cómo anular el registro del proveedor de eventos y liberarlo.</span><span class="sxs-lookup"><span data-stu-id="5693a-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="5693a-142">Limpie el servidor COM.</span><span class="sxs-lookup"><span data-stu-id="5693a-142">Clean up the COM server.</span></span>

    <span data-ttu-id="5693a-143">En el ejemplo de código siguiente se muestra cómo anular la inicialización de la biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="5693a-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5693a-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5693a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5693a-145">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="5693a-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="5693a-146">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="5693a-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="5693a-147">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="5693a-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



