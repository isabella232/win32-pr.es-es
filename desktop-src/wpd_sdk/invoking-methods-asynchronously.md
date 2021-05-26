---
description: Invocación asincrónica de métodos de servicio
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Invocación asincrónica de métodos de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423855"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="8cd08-103">Invocación asincrónica de métodos de servicio</span><span class="sxs-lookup"><span data-stu-id="8cd08-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="8cd08-104">La aplicación WpdServiceApiSample incluye código que muestra cómo una aplicación puede invocar los métodos de servicio de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8cd08-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="8cd08-105">En este ejemplo se usan las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="8cd08-105">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="8cd08-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="8cd08-106">Interface</span></span>    | <span data-ttu-id="8cd08-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cd08-107">Description</span></span>          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cd08-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="8cd08-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="8cd08-109">Se usa para recuperar la **interfaz IPortableDeviceServiceMethods** para invocar métodos en un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="8cd08-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="8cd08-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="8cd08-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="8cd08-111">Se usa para invocar un método de servicio.</span><span class="sxs-lookup"><span data-stu-id="8cd08-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="8cd08-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8cd08-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="8cd08-113">Se usa para contener los parámetros del método saliente y los resultados del método entrante.</span><span class="sxs-lookup"><span data-stu-id="8cd08-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="8cd08-114">Puede ser **NULL si** el método no requiere ningún parámetro o devuelve resultados.</span><span class="sxs-lookup"><span data-stu-id="8cd08-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="8cd08-115">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="8cd08-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="8cd08-116">Implementado por la aplicación para recibir los resultados del método cuando se ha completado un método.</span><span class="sxs-lookup"><span data-stu-id="8cd08-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="8cd08-117">Cuando el usuario elige la opción "10" en la línea de comandos, la aplicación invoca el método **InvokeMethodsAsync** que se encuentra en el módulo ServiceMethods.cpp.</span><span class="sxs-lookup"><span data-stu-id="8cd08-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="8cd08-118">Tenga en cuenta que antes de invocar los métodos, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="8cd08-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="8cd08-119">Los métodos de servicio encapsulan la funcionalidad que cada servicio define e implementa.</span><span class="sxs-lookup"><span data-stu-id="8cd08-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="8cd08-120">Son únicos para cada tipo de servicio y se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="8cd08-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="8cd08-121">Por ejemplo, el servicio Contacts define un método **BeginSync** al que las aplicaciones llaman para preparar el dispositivo para sincronizar objetos Contact y un método **EndSync** para notificar al dispositivo que se ha completado la sincronización.</span><span class="sxs-lookup"><span data-stu-id="8cd08-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="8cd08-122">Las aplicaciones ejecutan un método de servicio de dispositivo portátil llamando [**a IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="8cd08-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="8cd08-123">Los métodos de servicio no deben confundirse con los comandos de WPD.</span><span class="sxs-lookup"><span data-stu-id="8cd08-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="8cd08-124">Los comandos WPD forman parte de la interfaz de controlador de dispositivos (DDI) WPD estándar y son el mecanismo para la comunicación entre una aplicación WPD y el controlador.</span><span class="sxs-lookup"><span data-stu-id="8cd08-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="8cd08-125">Los comandos están predefinidos, agrupados por categorías (por ejemplo, **WPD \_ CATEGORY \_ COMMON)** y se representan mediante una **estructura PROPERTYKEY.**</span><span class="sxs-lookup"><span data-stu-id="8cd08-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="8cd08-126">Una aplicación envía comandos al controlador de dispositivo mediante una llamada [**a IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="8cd08-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="8cd08-127">Para obtener más información, vea el tema Comandos.</span><span class="sxs-lookup"><span data-stu-id="8cd08-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="8cd08-128">El **método InvokeMethodsAsync** invoca [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una [**interfaz IPortableDeviceServiceMethods.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)</span><span class="sxs-lookup"><span data-stu-id="8cd08-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="8cd08-129">Con esta interfaz, invoca la función auxiliar **InvokeMethodAsync** dos veces; una vez para **el método BeginSync** y otra para **el método EndSync.**</span><span class="sxs-lookup"><span data-stu-id="8cd08-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="8cd08-130">En este ejemplo, , **InvokeMethodAsync** espera indefinidamente a que se señale un evento global cuando se llama a [**IPortableDeviceServiceMethodCallback::OnComplete.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete)</span><span class="sxs-lookup"><span data-stu-id="8cd08-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="8cd08-131">El código siguiente usa el **método InvokeMethodsAsync.**</span><span class="sxs-lookup"><span data-stu-id="8cd08-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



<span data-ttu-id="8cd08-132">La función auxiliar **InvokeMethodAsync** hace lo siguiente para cada método que invoca:</span><span class="sxs-lookup"><span data-stu-id="8cd08-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="8cd08-133">Crea un identificador de evento global que supervisa para determinar la finalización del método.</span><span class="sxs-lookup"><span data-stu-id="8cd08-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="8cd08-134">Crea un **objeto CMethodCallback** que se proporciona como argumento para [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span><span class="sxs-lookup"><span data-stu-id="8cd08-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="8cd08-135">Llama al **método IPortableDeviceServiceMethods::InvokeAsync** para invocar el método especificado.</span><span class="sxs-lookup"><span data-stu-id="8cd08-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="8cd08-136">Supervisa el identificador global de eventos para su finalización.</span><span class="sxs-lookup"><span data-stu-id="8cd08-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="8cd08-137">Realiza la limpieza.</span><span class="sxs-lookup"><span data-stu-id="8cd08-137">Performs cleanup.</span></span>

<span data-ttu-id="8cd08-138">La **clase CMethodCallback** muestra cómo una aplicación puede implementar [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span><span class="sxs-lookup"><span data-stu-id="8cd08-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="8cd08-139">La implementación de **OnComplete** en esta clase indica un evento para notificar a la aplicación que el método de servicio se ha completado.</span><span class="sxs-lookup"><span data-stu-id="8cd08-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="8cd08-140">Además del método **OnComplete,** esta clase implementa **AddRef**, **QueryInterface** y **Release**, que se usan para mantener el recuento de referencias del objeto y las interfaces que implementa.</span><span class="sxs-lookup"><span data-stu-id="8cd08-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a><span data-ttu-id="8cd08-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cd08-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd08-142">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="8cd08-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="8cd08-143">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="8cd08-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="8cd08-144">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="8cd08-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="8cd08-145">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="8cd08-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
