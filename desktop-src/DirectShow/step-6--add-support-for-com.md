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
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="d853a-105">Paso 6.</span><span class="sxs-lookup"><span data-stu-id="d853a-105">Step 6.</span></span> <span data-ttu-id="d853a-106">Agregar compatibilidad con COM</span><span class="sxs-lookup"><span data-stu-id="d853a-106">Add Support for COM</span></span>

<span data-ttu-id="d853a-107">Este es el paso 6 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d853a-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="d853a-108">El último paso es agregar compatibilidad con COM.</span><span class="sxs-lookup"><span data-stu-id="d853a-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="d853a-109">Recuento de referencias</span><span class="sxs-lookup"><span data-stu-id="d853a-109">Reference Counting</span></span>

<span data-ttu-id="d853a-110">No es necesario implementar [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) o [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d853a-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d853a-111">Todas las clases de filtro y anclar derivan de [**CUnknown**](cunknown.md), que controla el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d853a-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="d853a-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="d853a-112">QueryInterface</span></span>

<span data-ttu-id="d853a-113">Todas las clases de filtro y anclar implementan [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para las interfaces COM que heredan.</span><span class="sxs-lookup"><span data-stu-id="d853a-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="d853a-114">Por ejemplo, [**CTransformFilter**](ctransformfilter.md) hereda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (a través [**de CBaseFilter).**](cbasefilter.md)</span><span class="sxs-lookup"><span data-stu-id="d853a-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="d853a-115">Si el filtro no expone ninguna interfaz adicional, no tiene que hacer nada más.</span><span class="sxs-lookup"><span data-stu-id="d853a-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="d853a-116">Para exponer interfaces adicionales, invalide el [**método CUnknown::NonDelegatingQueryInterface.**](cunknown-nondelegatingqueryinterface.md)</span><span class="sxs-lookup"><span data-stu-id="d853a-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="d853a-117">Por ejemplo, suponga que el filtro implementa una interfaz personalizada denominada IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="d853a-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="d853a-118">Para exponer esta interfaz a los clientes, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d853a-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="d853a-119">Derive la clase de filtro de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="d853a-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="d853a-120">Coloque la [**macro DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la sección de declaración pública.</span><span class="sxs-lookup"><span data-stu-id="d853a-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="d853a-121">Invalide [**NonDelegatingQueryInterface para**](cunknown-nondelegatingqueryinterface.md) buscar el IID de la interfaz y devolver un puntero al filtro.</span><span class="sxs-lookup"><span data-stu-id="d853a-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="d853a-122">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="d853a-122">The following code shows these steps:</span></span>


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



<span data-ttu-id="d853a-123">Para obtener más información, [vea How to Implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d853a-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="d853a-124">Creación de objetos</span><span class="sxs-lookup"><span data-stu-id="d853a-124">Object Creation</span></span>

<span data-ttu-id="d853a-125">Si tiene previsto empaquetar el filtro en un archivo DLL y hacer que esté disponible para otros clientes, debe admitir [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y otras funciones COM relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d853a-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="d853a-126">La biblioteca de clases base implementa la mayor parte de esto; solo tiene que proporcionar información sobre el filtro.</span><span class="sxs-lookup"><span data-stu-id="d853a-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="d853a-127">En esta sección se proporciona una breve introducción a lo que se debe hacer.</span><span class="sxs-lookup"><span data-stu-id="d853a-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="d853a-128">Para obtener más información, [vea How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d853a-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="d853a-129">En primer lugar, escriba un método de clase estático que devuelva una nueva instancia del filtro.</span><span class="sxs-lookup"><span data-stu-id="d853a-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="d853a-130">Puede dar a este método el nombre que quiera, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d853a-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="d853a-131">A continuación, declare una matriz global [**de instancias de clase CFactoryTemplate,**](cfactorytemplate.md) denominada g *\_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="d853a-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="d853a-132">Cada **clase CFactoryTemplate** contiene información del Registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="d853a-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="d853a-133">Varios filtros pueden residir en un solo archivo DLL; simplemente incluya entradas **adicionales de CFactoryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="d853a-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="d853a-134">También puede declarar otros objetos COM, como páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d853a-134">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="d853a-135">Defina un entero global denominado *g \_ cTemplates* cuyo valor sea igual a la longitud de la matriz *g \_ Templates:*</span><span class="sxs-lookup"><span data-stu-id="d853a-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="d853a-136">Por último, implemente las funciones de registro de DLL.</span><span class="sxs-lookup"><span data-stu-id="d853a-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="d853a-137">En el ejemplo siguiente se muestra la implementación mínima para estas funciones:</span><span class="sxs-lookup"><span data-stu-id="d853a-137">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="d853a-138">Filtrar entradas del Registro</span><span class="sxs-lookup"><span data-stu-id="d853a-138">Filter Registry Entries</span></span>

<span data-ttu-id="d853a-139">En los ejemplos anteriores se muestra cómo registrar el CLSID de un filtro para COM.</span><span class="sxs-lookup"><span data-stu-id="d853a-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="d853a-140">Para muchos filtros, esto es suficiente.</span><span class="sxs-lookup"><span data-stu-id="d853a-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="d853a-141">A continuación, se espera que el cliente cree el filtro mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y lo agregue al gráfico de filtros mediante una llamada a [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="d853a-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="d853a-142">Sin embargo, en algunos casos, es posible que desee proporcionar información adicional sobre el filtro en el Registro.</span><span class="sxs-lookup"><span data-stu-id="d853a-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="d853a-143">Esta información hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d853a-143">This information does the following:</span></span>

-   <span data-ttu-id="d853a-144">Permite a los clientes detectar el filtro mediante [el Asignador de filtros](filter-mapper.md) o el [Enumerador de dispositivos del sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="d853a-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="d853a-145">Permite que el Administrador de gráficos de filtros detecte el filtro durante la creación automática del grafo.</span><span class="sxs-lookup"><span data-stu-id="d853a-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="d853a-146">En el ejemplo siguiente se registra el filtro del codificador RLE en la categoría de vídeos.</span><span class="sxs-lookup"><span data-stu-id="d853a-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="d853a-147">Para más información, [consulte Registro de filtros de DirectShow.](how-to-register-directshow-filters.md)</span><span class="sxs-lookup"><span data-stu-id="d853a-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="d853a-148">Asegúrese de leer la sección [Directrices](guidelines-for-registering-filters.md)para registrar filtros , que describe las prácticas recomendadas para el registro de filtros.</span><span class="sxs-lookup"><span data-stu-id="d853a-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="d853a-149">Además, los filtros no tienen que empaquetarse dentro de archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="d853a-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="d853a-150">En algunos casos, podría escribir un filtro especializado diseñado solo para una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="d853a-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="d853a-151">En ese caso, puede compilar la clase de filtro directamente en la aplicación y crearla con el operador , como se `new` muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d853a-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d853a-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d853a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d853a-153">Conexión inteligente</span><span class="sxs-lookup"><span data-stu-id="d853a-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="d853a-154">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d853a-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d853a-155">Escribir filtros de transformación</span><span class="sxs-lookup"><span data-stu-id="d853a-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
