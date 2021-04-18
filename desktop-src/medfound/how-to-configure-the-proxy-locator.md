---
description: Cómo configurar el localizador de proxy
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Cómo configurar el localizador de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b383dda9ac78b2c62aa8481a09cc5c0d7b3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715445"
---
# <a name="how-to-configure-the-proxy-locator"></a><span data-ttu-id="68c71-103">Cómo configurar el localizador de proxy</span><span class="sxs-lookup"><span data-stu-id="68c71-103">How to Configure the Proxy Locator</span></span>

<span data-ttu-id="68c71-104">La aplicación puede cambiar la configuración predeterminada del localizador de proxy mediante el establecimiento de la propiedad [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) en el objeto de generador de localizador de proxy implementado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68c71-104">The application can change the default configuration of the proxy locator by setting the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property to the proxy locator factory object that is implemented by the application.</span></span> <span data-ttu-id="68c71-105">Cuando la aplicación llama a los métodos de resolución de origen para crear el origen de red, Media Foundation llama al generador de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="68c71-105">When the application calls source resolver methods to create the network source, Media Foundation calls the proxy locator factory.</span></span> <span data-ttu-id="68c71-106">Este objeto crea el localizador de proxy con la configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="68c71-106">This object creates the proxy locator with custom configuration.</span></span>

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a><span data-ttu-id="68c71-107">Para cambiar la configuración predeterminada del localizador de proxy</span><span class="sxs-lookup"><span data-stu-id="68c71-107">To change the default configuration setting of the proxy locator</span></span>

1.  <span data-ttu-id="68c71-108">Implemente la interfaz [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="68c71-108">Implement the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
2.  <span data-ttu-id="68c71-109">En el método [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="68c71-109">In the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method, do the following:</span></span>
    1.  <span data-ttu-id="68c71-110">Cree un almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="68c71-110">Create a property store.</span></span>
    2.  <span data-ttu-id="68c71-111">Establezca la configuración del localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="68c71-111">Set the configuration settings for the proxy locator.</span></span> <span data-ttu-id="68c71-112">Para obtener información acerca de esta configuración, consulte [configuración del localizador de proxy](proxy-locator-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="68c71-112">For information about these settings, see [Proxy Locator Configuration Settings](proxy-locator-configuration-settings.md).</span></span>
    3.  <span data-ttu-id="68c71-113">Llame a la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="68c71-113">Call the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="68c71-114">Pase el almacén de propiedades y el protocolo.</span><span class="sxs-lookup"><span data-stu-id="68c71-114">Pass in the property store and the protocol.</span></span> <span data-ttu-id="68c71-115">El protocolo se especifica en el parámetro *pszProtocol* de [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span><span class="sxs-lookup"><span data-stu-id="68c71-115">The protocol is specified in the *pszProtocol* parameter of [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span></span>
3.  <span data-ttu-id="68c71-116">Cree una instancia de la clase de generador de localizador proxy y obtenga un puntero a su interfaz [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="68c71-116">Create an instance of your proxy locator factory class and get a pointer to its [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
4.  <span data-ttu-id="68c71-117">Cree otro almacén de propiedades y establezca el valor de la propiedad [**MFNETSOURCE \_ PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) en el puntero [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) del paso 3.</span><span class="sxs-lookup"><span data-stu-id="68c71-117">Create another property store and set the value of the [**MFNETSOURCE\_PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) property equal to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer from step 3.</span></span>
5.  <span data-ttu-id="68c71-118">Al crear el origen de red, pase el almacén de propiedades en el parámetro *pProps* de los métodos de resolución de origen como [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="68c71-118">When you create the network source, pass the property store in the *pProps* parameter of the source resolver methods such as [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

## <a name="example"></a><span data-ttu-id="68c71-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68c71-119">Example</span></span>

<span data-ttu-id="68c71-120">En el ejemplo de código siguiente se implementa la interfaz [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="68c71-120">The following code example implements the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span> <span data-ttu-id="68c71-121">El método [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) crea una instancia del localizador de proxy predeterminado y la configura para que funcione en modo de detección automática.</span><span class="sxs-lookup"><span data-stu-id="68c71-121">The [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method creates an instance of the default proxy locator, and configures it to operate in auto-detect mode.</span></span>


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



<span data-ttu-id="68c71-122">En el ejemplo siguiente se muestra cómo pasar el puntero [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) al origen de red.</span><span class="sxs-lookup"><span data-stu-id="68c71-122">The next example shows how to pass the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer to the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="68c71-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68c71-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68c71-124">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="68c71-124">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



