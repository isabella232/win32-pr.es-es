---
description: Cargadores de topología personalizados
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Cargadores de topología personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ca9cf393b83693199cea984183bf88186f74322ed816352e3c43d19a6e880b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880390"
---
# <a name="custom-topology-loaders"></a>Cargadores de topología personalizados

Cuando una aplicación pone en cola una topología parcial en la sesión multimedia, la sesión multimedia usa un cargador de topologías para resolver la topología. De forma predeterminada, la sesión multimedia usa la implementación Media Foundation estándar del cargador de topologías, pero también puede proporcionar una implementación personalizada. Esto le proporciona más control sobre la topología final. Un cargador de topologías personalizado debe implementar [**la interfaz DETOPOLoader.**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)

Para establecer un cargador de topologías personalizado en la sesión multimedia, haga lo siguiente:

1.  Cree un almacén de atributos vacío mediante una [**llamada a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Establezca el [**atributo MF \_ SESSION \_ TOPOLOADER**](mf-session-topoloader-attribute.md) en el almacén de atributos. El valor del atributo es el CLSID del cargador personalizado.
3.  Llame [**a MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia para contenido no protegido o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para crear la sesión multimedia dentro de la ruta de acceso multimedia protegida (PMP).

> [!Note]  
> Para usar un cargador de topologías personalizado dentro del PMP, el cargador de topologías debe ser un componente de confianza. Para obtener más información, vea [Ruta de acceso de medios protegidos.](protected-media-path.md)

 

El código siguiente muestra cómo establecer un cargador de topologías personalizado en la sesión multimedia.


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



No es necesario implementar todo el algoritmo de carga de topologías en el cargador de topologías. Como alternativa, puede encapsular el cargador Media Foundation topología estándar. En la implementación del método [**IMFTopoLoader::Load,**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) modifique la topología según sea necesario y pase la topología modificada al cargador de topologías estándar. A continuación, el cargador de topologías estándar completa la topología. También puede modificar la topología completada antes de devolverla a la sesión multimedia.

El código siguiente muestra el esquema general de este enfoque. No muestra ningún detalle del método [**Load,**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) ya que dependerá de los requisitos concretos de la aplicación.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Creación de topología avanzada](advanced-topology-building.md)
</dt> </dl>

 

 



