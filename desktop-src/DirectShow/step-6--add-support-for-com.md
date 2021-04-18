---
description: Paso 6.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Paso 6. Agregar compatibilidad con COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e477cc22650604bce623874c0afbba1063609e44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688221"
---
# <a name="step-6-add-support-for-com"></a>Paso 6. Agregar compatibilidad con COM

Este es el paso 6 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

El paso final consiste en agregar compatibilidad con COM.

## <a name="reference-counting"></a>Recuento de referencias

No es necesario implementar [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) o [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todas las clases Filter y PIN derivan de [**CUnknown**](cunknown.md), que controla el recuento de referencias.

## <a name="queryinterface"></a>QueryInterface

Todas las clases Filter y PIN implementan [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para todas las interfaces com que heredan. Por ejemplo, [**CTransformFilter**](ctransformfilter.md) hereda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (a través de [**CBaseFilter**](cbasefilter.md)). Si el filtro no expone ninguna interfaz adicional, no es necesario hacer nada más.

Para exponer interfaces adicionales, invalide el método [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) . Por ejemplo, supongamos que el filtro implementa una interfaz personalizada denominada IMyCustomInterface. Para exponer esta interfaz a los clientes, haga lo siguiente:

-   Derive la clase de filtro de esa interfaz.
-   Coloque la macro [**declare \_ IUNKNOWN**](declare-iunknown.md) en la sección declaración pública.
-   Invalide [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para comprobar el IID de la interfaz y devolver un puntero al filtro.

El siguiente código muestra estos pasos:


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



Para obtener más información, vea [How to implement IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Creación de objetos

Si planea empaquetar el filtro en un archivo DLL y ponerlo a disposición de otros clientes, debe admitir [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y otras funciones com relacionadas. La biblioteca de clases base implementa la mayor parte de esto; solo tiene que proporcionar información sobre el filtro. En esta sección se proporciona una breve descripción de lo que hay que hacer. Para obtener más información, vea [Cómo crear un archivo dll de filtro de DirectShow](how-to-create-a-dll.md).

En primer lugar, escriba un método de clase estática que devuelva una nueva instancia del filtro. Puede asignar el nombre que desee a este método, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



A continuación, declare una matriz global de instancias de la clase [**CFactoryTemplate**](cfactorytemplate.md) , denominada *g \_ templates*. Cada clase **CFactoryTemplate** contiene información del registro para un filtro. Varios filtros pueden residir en un único archivo DLL; simplemente incluya entradas **CFactoryTemplate** adicionales. También puede declarar otros objetos COM, como páginas de propiedades.


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



Defina un entero global denominado *g \_ cTemplates* cuyo valor sea igual a la longitud de la matriz de *\_ plantillas g* :


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Por último, implemente las funciones de registro de archivos DLL. En el ejemplo siguiente se muestra la implementación mínima para estas funciones:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a>Filtrar entradas del registro

En los ejemplos anteriores se muestra cómo registrar el CLSID de un filtro para COM. Para muchos filtros, esto es suficiente. A continuación, se espera que el cliente cree el filtro mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y lo agregue al gráfico de filtros mediante una llamada a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter). En algunos casos, sin embargo, es posible que desee proporcionar información adicional sobre el filtro en el registro. Esta información hace lo siguiente:

-   Permite a los clientes detectar el filtro mediante el [asignador de filtros](filter-mapper.md) o el [enumerador de dispositivos del sistema](system-device-enumerator.md).
-   Permite al administrador de gráficos de filtro detectar el filtro durante la creación automática de gráficos.

En el ejemplo siguiente se registra el filtro del codificador RLE en la categoría compresor de vídeo. Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md). Asegúrese de leer la sección [directrices para registrar filtros](guidelines-for-registering-filters.md), que describe las prácticas recomendadas para el registro de filtros.


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



Además, no es necesario empaquetar los filtros dentro de los archivos dll. En algunos casos, puede escribir un filtro especializado que esté diseñado únicamente para una aplicación específica. En ese caso, puede compilar la clase de filtro directamente en la aplicación y crearla con el `new` operador, como se muestra en el ejemplo siguiente:


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión inteligente](intelligent-connect.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> <dt>

[Escribir filtros de transformación](writing-transform-filters.md)
</dt> </dl>

 

 
