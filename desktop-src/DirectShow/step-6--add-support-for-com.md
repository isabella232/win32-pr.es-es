---
description: Agregue compatibilidad con COM como parte de la escritura de un filtro de transformación. Este es el paso final de este tutorial.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Paso 6. Agregar compatibilidad con COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406778"
---
# <a name="step-6-add-support-for-com"></a>Paso 6. Agregar compatibilidad con COM

Este es el paso 6 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

El último paso es agregar compatibilidad con COM.

## <a name="reference-counting"></a>Recuento de referencias

No es necesario implementar [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) o [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todas las clases de filtro y anclar derivan de [**CUnknown**](cunknown.md), que controla el recuento de referencias.

## <a name="queryinterface"></a>QueryInterface

Todas las clases de filtro y anclar implementan [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para las interfaces COM que heredan. Por ejemplo, [**CTransformFilter**](ctransformfilter.md) hereda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (a través [**de CBaseFilter).**](cbasefilter.md) Si el filtro no expone ninguna interfaz adicional, no tiene que hacer nada más.

Para exponer interfaces adicionales, invalide el [**método CUnknown::NonDelegatingQueryInterface.**](cunknown-nondelegatingqueryinterface.md) Por ejemplo, suponga que el filtro implementa una interfaz personalizada denominada IMyCustomInterface. Para exponer esta interfaz a los clientes, haga lo siguiente:

-   Derive la clase de filtro de esa interfaz.
-   Coloque la [**macro DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la sección de declaración pública.
-   Invalide [**NonDelegatingQueryInterface para**](cunknown-nondelegatingqueryinterface.md) buscar el IID de la interfaz y devolver un puntero al filtro.

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



Para obtener más información, [vea How to Implement IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Creación de objetos

Si tiene previsto empaquetar el filtro en un archivo DLL y hacer que esté disponible para otros clientes, debe admitir [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y otras funciones COM relacionadas. La biblioteca de clases base implementa la mayor parte de esto; solo tiene que proporcionar información sobre el filtro. En esta sección se proporciona una breve introducción a lo que se debe hacer. Para obtener más información, [vea How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).

En primer lugar, escriba un método de clase estático que devuelva una nueva instancia del filtro. Puede dar a este método el nombre que quiera, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:


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



A continuación, declare una matriz global [**de instancias de clase CFactoryTemplate,**](cfactorytemplate.md) denominada g *\_ Templates*. Cada **clase CFactoryTemplate** contiene información del Registro para un filtro. Varios filtros pueden residir en un solo archivo DLL; simplemente incluya entradas **adicionales de CFactoryTemplate.** También puede declarar otros objetos COM, como páginas de propiedades.


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



Defina un entero global denominado *g \_ cTemplates* cuyo valor sea igual a la longitud de la matriz *g \_ Templates:*


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Por último, implemente las funciones de registro de DLL. En el ejemplo siguiente se muestra la implementación mínima para estas funciones:


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



## <a name="filter-registry-entries"></a>Filtrar entradas del Registro

En los ejemplos anteriores se muestra cómo registrar el CLSID de un filtro para COM. Para muchos filtros, esto es suficiente. A continuación, se espera que el cliente cree el filtro mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y lo agregue al gráfico de filtros mediante una llamada a [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter). Sin embargo, en algunos casos, es posible que desee proporcionar información adicional sobre el filtro en el Registro. Esta información hace lo siguiente:

-   Permite a los clientes detectar el filtro mediante [el Asignador de filtros](filter-mapper.md) o el [Enumerador de dispositivos del sistema](system-device-enumerator.md).
-   Permite que el Administrador de gráficos de filtros detecte el filtro durante la creación automática del grafo.

En el ejemplo siguiente se registra el filtro del codificador RLE en la categoría de vídeos. Para más información, [consulte Registro de filtros de DirectShow.](how-to-register-directshow-filters.md) Asegúrese de leer la sección [Directrices](guidelines-for-registering-filters.md)para registrar filtros , que describe las prácticas recomendadas para el registro de filtros.


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



Además, los filtros no tienen que empaquetarse dentro de archivos DLL. En algunos casos, podría escribir un filtro especializado diseñado solo para una aplicación específica. En ese caso, puede compilar la clase de filtro directamente en la aplicación y crearla con el operador , como se `new` muestra en el ejemplo siguiente:


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

 

 
