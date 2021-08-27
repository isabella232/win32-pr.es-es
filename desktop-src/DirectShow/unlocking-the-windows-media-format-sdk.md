---
description: Desbloqueo del SDK Windows Media Format
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Desbloqueo del SDK Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1f332711e9fd12c9b0ff1f789438d051487b81711f157ae1024a8e47973386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078665"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>Desbloqueo del SDK Windows Media Format

Para acceder a la versión 7 o 7.1 del SDK de formato multimedia de Windows, una aplicación debe proporcionar un certificado de software, también denominado clave, en tiempo de ejecución. Esta clave está contenida en una biblioteca estática denominada wmstub.lib a la que la aplicación se vincula en tiempo de compilación. Solo se necesita una clave individualizada para crear o leer archivos protegidos con DRM. Los archivos que no son DRM se pueden crear mediante la biblioteca estática proporcionada con Windows SDK de formato multimedia. Para más información sobre cómo obtener la clave DRM, consulte el sdk Windows Media Format. Una DirectShow aplicación proporciona su certificado a WM ASF Writer cuando se agrega al gráfico de filtros. La aplicación debe registrarse como proveedor de claves mediante las interfaces COM **IServiceProvider** **e IObjectWithSite.** Con esta técnica, la aplicación implementa una clase de proveedor de claves derivada de **IServiceProvider**. Esta clase implementa los tres métodos COM estándar:**AddRef,** **QueryInterface** y **Release,** junto con un método adicional, **QueryService**, al que llama el administrador de gráficos de filtro. **QueryService** llama Windows método [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) del SDK de formato multimedia y devuelve al administrador de gráficos de filtro un puntero al certificado que se creó. Si el certificado es válido, el administrador de gráficos de filtro permite que el proceso de creación de grafos continúe.

> [!Note]  
> Para compilar una aplicación, incluya Wmsdkidl.h para el prototipo de [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))y vincule a la biblioteca Wmstub.lib.

 

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

[Creación de archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
