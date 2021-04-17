---
description: Desbloqueo del SDK de Windows Media Format
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Desbloqueo del SDK de Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689661"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>Desbloqueo del SDK de Windows Media Format

Para tener acceso a la versión 7 o 7,1 del SDK de Windows Media Format, una aplicación debe proporcionar un certificado de software, también denominado clave, en tiempo de ejecución. Esta clave se encuentra en una biblioteca estática denominada wmstub. lib a la que se vincula la aplicación en tiempo de compilación. Una clave individualizada solo es necesaria para crear o leer archivos protegidos con DRM. Los archivos no DRM se pueden crear mediante la biblioteca estática que se proporciona con el SDK de Windows Media Format. Para obtener más información sobre cómo obtener la clave DRM, vea el SDK de Windows Media Format. Una aplicación de DirectShow proporciona su certificado al escritor ASF de WM cuando se agrega al gráfico de filtro. La aplicación debe registrarse como proveedor de claves mediante las interfaces COM **IServiceProvider** y **IObjectWithSite** . Con esta técnica, la aplicación implementa una clase de proveedor de claves derivada de **IServiceProvider**. Esta clase implementa los tres métodos COM estándar:**AddRef**, **QueryInterface** y **Release**, junto con un método adicional, **QueryService**, al que llama el administrador de gráficos de filtro. **QueryService** llama al método [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) de Windows Media Format SDK y vuelve al administrador de gráficos de filtro un puntero al certificado que se creó. Si el certificado es válido, el administrador de gráficos de filtros permite que continúe el proceso de creación de gráficos.

> [!Note]  
> Para compilar una aplicación, incluya Wmsdkidl. h para el prototipo de [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))y vincúlelo a la biblioteca Wmstub. lib.

 

En el ejemplo de código siguiente se muestran los pasos básicos de este proceso:


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
