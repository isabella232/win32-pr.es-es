---
description: Microsoft Media Foundation usa una combinación de construcciones COM, pero no es una API totalmente basada en COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation y COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721350"
---
# <a name="media-foundation-and-com"></a><span data-ttu-id="ac5e5-103">Media Foundation y COM</span><span class="sxs-lookup"><span data-stu-id="ac5e5-103">Media Foundation and COM</span></span>

<span data-ttu-id="ac5e5-104">Microsoft Media Foundation usa una combinación de construcciones COM, pero no es una API totalmente basada en COM.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="ac5e5-105">En este tema se describe la interacción entre COM y Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="ac5e5-106">También define algunos procedimientos recomendados para desarrollar componentes de complemento de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="ac5e5-107">Estos procedimientos pueden ayudarle a evitar algunos errores de programación comunes pero sutiles.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="ac5e5-108">Prácticas recomendadas para aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ac5e5-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="ac5e5-109">Prácticas recomendadas para componentes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac5e5-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="ac5e5-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="ac5e5-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="ac5e5-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac5e5-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="ac5e5-112">Prácticas recomendadas para aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ac5e5-112">Best Practices for Applications</span></span>

<span data-ttu-id="ac5e5-113">En Media Foundation, las [colas de trabajo](work-queues.md)controlan el procesamiento asincrónico y las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="ac5e5-114">Las colas de trabajo siempre tienen subprocesos de Apartamento multiproceso (MTA), por lo que una aplicación tendrá una implementación más sencilla si se ejecuta también en un subproceso MTA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="ac5e5-115">Por lo tanto, se recomienda llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con la marca de **COinit \_ multithreaded** .</span><span class="sxs-lookup"><span data-stu-id="ac5e5-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="ac5e5-116">Media Foundation no calcula los objetos de contenedor uniproceso (STA) para los subprocesos de la cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="ac5e5-117">Tampoco garantiza que se mantengan las invariantes de STA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="ac5e5-118">Por lo tanto, una aplicación STA debe tener cuidado de no pasar objetos STA o proxies a Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="ac5e5-119">Los objetos que son solo STA no se admiten en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="ac5e5-120">Si tiene un proxy STA a un objeto MTA o de subprocesamiento libre, el objeto se puede serializar en un proxy MTA mediante una devolución de llamada de cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="ac5e5-121">La función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) puede devolver un puntero sin formato o un proxy STA, dependiendo del modelo de objetos definido en el registro para ese CLSID.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="ac5e5-122">Si se devuelve un proxy STA, no debe pasar el puntero a una API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="ac5e5-123">Por ejemplo, supongamos que desea pasar un puntero **IPropertyStore** al método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="ac5e5-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="ac5e5-124">Puede llamar a **PSCreateMemoryPropertyStore** para crear el puntero **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="ac5e5-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="ac5e5-125">Si llama a desde un STA, debe serializar el puntero antes de pasarlo a **BeginCreateObjectFromURL**.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="ac5e5-126">En el código siguiente se muestra cómo calcular las referencias de un proxy STA a una API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



<span data-ttu-id="ac5e5-127">Para obtener más información acerca de la tabla de la interfaz global, vea [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="ac5e5-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="ac5e5-128">Si usa Media Foundation en proceso, los objetos devueltos de Media Foundation métodos y funciones son punteros directos al objeto.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="ac5e5-129">En el caso de Media Foundation entre procesos, estos objetos pueden ser proxies MTA y se deben calcular las referencias en un subproceso STA si es necesario.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="ac5e5-130">Del mismo modo, los objetos que se obtienen dentro de una devolución de llamada (por ejemplo, una topología del evento [MESessionTopologyStatus](mesessiontopologystatus.md) ) son punteros directos cuando Media Foundation se usa en proceso, pero son proxies MTA cuando Media Foundation se usa entre procesos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="ac5e5-131">El escenario más común para el uso de Media Foundation entre procesos es con la ruta de acceso a los [medios protegidos](protected-media-path.md) (PMP).</span><span class="sxs-lookup"><span data-stu-id="ac5e5-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="ac5e5-132">Sin embargo, estas notas se aplican a cualquier situación cuando se usan Media Foundation API a través de RPC.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="ac5e5-133">Todas las implementaciones de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) deben ser compatibles con MTA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="ac5e5-134">No es necesario que estos objetos sean objetos COM.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="ac5e5-135">Pero si son, no se pueden ejecutar en el STA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="ac5e5-136">La función [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) se invocará en un subproceso MTA workqueue y el objeto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) proporcionado será un puntero de objeto directo o un proxy MTA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="ac5e5-137">Prácticas recomendadas para componentes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac5e5-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="ac5e5-138">Hay dos categorías de objetos de Media Foundation que deben preocuparse de COM.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="ac5e5-139">Algunos componentes, como las transformaciones o los controladores de secuencias de bytes, son objetos COM completos creados por CLSID.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="ac5e5-140">Estos objetos deben seguir las reglas de los apartamentos COM, tanto en el proceso como en el Media Foundation entre procesos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="ac5e5-141">Otros componentes Media Foundation no son objetos COM completos, pero necesitan proxies COM para la reproducción entre procesos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="ac5e5-142">Los objetos de esta categoría incluyen orígenes de medios y objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="ac5e5-143">Estos objetos pueden omitir los problemas de apartamento si solo se van a utilizar para Media Foundation en proceso.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="ac5e5-144">Aunque no todos los objetos Media Foundation son objetos COM, todas las interfaces de Media Foundation derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="ac5e5-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="ac5e5-145">Por lo tanto, todos los objetos Media Foundation deben implementar **IUnknown** de acuerdo con las especificaciones com, incluidas las reglas para el recuento de referencias y [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="ac5e5-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="ac5e5-146">Todos los objetos contables de referencia también deben asegurarse de que [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) no permitirá que el módulo se descargue mientras los objetos persisten.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="ac5e5-147">Los componentes de Media Foundation no pueden ser objetos STA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="ac5e5-148">Muchos objetos Media Foundation no necesitan ser objetos COM.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="ac5e5-149">Pero si son, no se pueden ejecutar en el STA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="ac5e5-150">Todos los componentes de Media Foundation deben ser seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="ac5e5-151">Algunos objetos Media Foundation deben ser de subprocesamiento libre o independiente.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="ac5e5-152">En la tabla siguiente se especifican los requisitos para las implementaciones de interfaz personalizadas:</span><span class="sxs-lookup"><span data-stu-id="ac5e5-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="ac5e5-153">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ac5e5-153">Interface</span></span>                                                          | <span data-ttu-id="ac5e5-154">Category</span><span class="sxs-lookup"><span data-stu-id="ac5e5-154">Category</span></span>            | <span data-ttu-id="ac5e5-155">Apartamento obligatorio</span><span class="sxs-lookup"><span data-stu-id="ac5e5-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="ac5e5-156">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="ac5e5-157">Proxy entre procesos</span><span class="sxs-lookup"><span data-stu-id="ac5e5-157">Cross-process proxy</span></span> | <span data-ttu-id="ac5e5-158">Subproceso libre o neutro</span><span class="sxs-lookup"><span data-stu-id="ac5e5-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ac5e5-159">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="ac5e5-160">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="ac5e5-160">COM object</span></span>          | <span data-ttu-id="ac5e5-161">MTA</span><span class="sxs-lookup"><span data-stu-id="ac5e5-161">MTA</span></span>                      |
| [<span data-ttu-id="ac5e5-162">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="ac5e5-163">Proxy entre procesos</span><span class="sxs-lookup"><span data-stu-id="ac5e5-163">Cross-process proxy</span></span> | <span data-ttu-id="ac5e5-164">Subproceso libre o neutro</span><span class="sxs-lookup"><span data-stu-id="ac5e5-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ac5e5-165">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="ac5e5-166">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="ac5e5-166">COM object</span></span>          | <span data-ttu-id="ac5e5-167">Subproceso libre o neutro</span><span class="sxs-lookup"><span data-stu-id="ac5e5-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ac5e5-168">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="ac5e5-169">Proxy entre procesos</span><span class="sxs-lookup"><span data-stu-id="ac5e5-169">Cross-process proxy</span></span> | <span data-ttu-id="ac5e5-170">Subproceso libre o neutro</span><span class="sxs-lookup"><span data-stu-id="ac5e5-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ac5e5-171">**IMFSchemeHandler**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="ac5e5-172">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="ac5e5-172">COM object</span></span>          | <span data-ttu-id="ac5e5-173">MTA</span><span class="sxs-lookup"><span data-stu-id="ac5e5-173">MTA</span></span>                      |
| [<span data-ttu-id="ac5e5-174">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="ac5e5-175">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="ac5e5-175">COM object</span></span>          | <span data-ttu-id="ac5e5-176">Subproceso libre o neutro</span><span class="sxs-lookup"><span data-stu-id="ac5e5-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ac5e5-177">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="ac5e5-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="ac5e5-178">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="ac5e5-178">COM object</span></span>          | <span data-ttu-id="ac5e5-179">MTA</span><span class="sxs-lookup"><span data-stu-id="ac5e5-179">MTA</span></span>                      |



 

<span data-ttu-id="ac5e5-180">Puede haber requisitos adicionales en función de la implementación.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="ac5e5-181">Por ejemplo, si un receptor de medios implementa otra interfaz que permite que la aplicación realice llamadas de función directas al receptor, el receptor tendría que ser de subprocesamiento libre o neutro, de modo que pueda controlar llamadas directas entre procesos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="ac5e5-182">Cualquier objeto puede ser de subprocesamiento libre; en esta tabla se especifican los requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="ac5e5-183">La manera recomendada de implementar objetos independientes o de subprocesos libres es agregando el contador de referencias de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="ac5e5-184">Para obtener más información, consulte la documentación de MSDN en [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span><span class="sxs-lookup"><span data-stu-id="ac5e5-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="ac5e5-185">De acuerdo con el requisito de no pasar objetos STA o proxies a Media Foundation API, no es necesario que los objetos de subprocesamiento libre tengan que preocuparse por la serialización de punteros de entrada STA en componentes de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="ac5e5-186">Los componentes que utilizan la cola de trabajo de función larga (**\_ \_ \_ \_ función Long de cola de devolución de llamada MFASYNC**) deben tener más cuidado.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="ac5e5-187">Los subprocesos de la función Long workqueue crean su propio STA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="ac5e5-188">Los componentes que utilizan la función Long workqueue para las devoluciones de llamada deberían evitar la creación de objetos COM en estos subprocesos y deben tener cuidado de calcular las referencias de los servidores proxy en el STA según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="ac5e5-189">Resumen</span><span class="sxs-lookup"><span data-stu-id="ac5e5-189">Summary</span></span>

<span data-ttu-id="ac5e5-190">Las aplicaciones tendrán un tiempo más sencillo si interactúan con Media Foundation desde un subproceso MTA, pero es posible que tenga cuidado al usar Media Foundation desde un subproceso STA.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="ac5e5-191">Media Foundation no controla los componentes STA y las aplicaciones deben tener cuidado de no pasar objetos STA a Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="ac5e5-192">Algunos objetos tienen requisitos adicionales, especialmente objetos que se ejecutan en una situación entre procesos.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="ac5e5-193">Seguir estas instrucciones le ayudará a evitar errores COM, interbloqueos y retrasos inesperados en el procesamiento de medios.</span><span class="sxs-lookup"><span data-stu-id="ac5e5-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac5e5-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac5e5-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac5e5-195">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="ac5e5-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="ac5e5-196">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac5e5-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
