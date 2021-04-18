---
description: Cargadores de topología personalizados
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Cargadores de topología personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714930"
---
# <a name="custom-topology-loaders"></a><span data-ttu-id="d1bfe-103">Cargadores de topología personalizados</span><span class="sxs-lookup"><span data-stu-id="d1bfe-103">Custom Topology Loaders</span></span>

<span data-ttu-id="d1bfe-104">Cuando una aplicación pone en cola una topología parcial en la sesión multimedia, la sesión multimedia utiliza un cargador de topología para resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="d1bfe-105">De forma predeterminada, la sesión multimedia utiliza la implementación de Media Foundation estándar del cargador de topología, pero también puede proporcionar una implementación personalizada.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="d1bfe-106">Esto le proporciona más control sobre la topología final.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="d1bfe-107">Un cargador de topología personalizado debe implementar la interfaz [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="d1bfe-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="d1bfe-108">Para establecer un cargador de topología personalizado en la sesión multimedia, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1bfe-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="d1bfe-109">Cree un almacén de atributos vacío mediante una llamada a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="d1bfe-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="d1bfe-110">Establezca el [**atributo \_ \_ TOPOLOADER de la sesión MF**](mf-session-topoloader-attribute.md) en el almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="d1bfe-111">El valor del atributo es el CLSID del cargador personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="d1bfe-112">Llame a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión de medios para contenido no protegido, o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para crear la sesión multimedia dentro de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="d1bfe-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="d1bfe-113">Para usar un cargador de topología personalizado dentro de la PMP, el cargador de topología debe ser un componente de confianza.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="d1bfe-114">Para obtener más información, vea [ruta de acceso a medios protegidos](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="d1bfe-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="d1bfe-115">El código siguiente muestra cómo establecer un cargador de topología personalizado en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



<span data-ttu-id="d1bfe-116">No es necesario implementar el algoritmo de carga de topología completo en el cargador de topología.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="d1bfe-117">Como alternativa, puede ajustar el cargador de topología de Media Foundation estándar.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="d1bfe-118">En la implementación del método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , modifique la topología según sea necesario y pase la topología modificada al cargador de topología estándar.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="d1bfe-119">A continuación, el cargador de topologías estándar completa la topología.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="d1bfe-120">También puede modificar la topología completada antes de pasarla de nuevo a la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="d1bfe-121">En el código siguiente se muestra el esquema general de este enfoque.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="d1bfe-122">No muestra ningún detalle del método de [**carga**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , ya que dependerá de los requisitos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d1bfe-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a><span data-ttu-id="d1bfe-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1bfe-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1bfe-124">**MFCreateTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="d1bfe-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="d1bfe-125">Creación de topologías avanzadas</span><span class="sxs-lookup"><span data-stu-id="d1bfe-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



