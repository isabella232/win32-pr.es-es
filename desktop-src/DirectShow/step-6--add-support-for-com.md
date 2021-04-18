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
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="ffb50-104">Paso 6.</span><span class="sxs-lookup"><span data-stu-id="ffb50-104">Step 6.</span></span> <span data-ttu-id="ffb50-105">Agregar compatibilidad con COM</span><span class="sxs-lookup"><span data-stu-id="ffb50-105">Add Support for COM</span></span>

<span data-ttu-id="ffb50-106">Este es el paso 6 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ffb50-106">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="ffb50-107">El paso final consiste en agregar compatibilidad con COM.</span><span class="sxs-lookup"><span data-stu-id="ffb50-107">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="ffb50-108">Recuento de referencias</span><span class="sxs-lookup"><span data-stu-id="ffb50-108">Reference Counting</span></span>

<span data-ttu-id="ffb50-109">No es necesario implementar [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) o [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="ffb50-109">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="ffb50-110">Todas las clases Filter y PIN derivan de [**CUnknown**](cunknown.md), que controla el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="ffb50-110">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="ffb50-111">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="ffb50-111">QueryInterface</span></span>

<span data-ttu-id="ffb50-112">Todas las clases Filter y PIN implementan [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para todas las interfaces com que heredan.</span><span class="sxs-lookup"><span data-stu-id="ffb50-112">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="ffb50-113">Por ejemplo, [**CTransformFilter**](ctransformfilter.md) hereda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (a través de [**CBaseFilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="ffb50-113">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="ffb50-114">Si el filtro no expone ninguna interfaz adicional, no es necesario hacer nada más.</span><span class="sxs-lookup"><span data-stu-id="ffb50-114">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="ffb50-115">Para exponer interfaces adicionales, invalide el método [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb50-115">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="ffb50-116">Por ejemplo, supongamos que el filtro implementa una interfaz personalizada denominada IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="ffb50-116">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="ffb50-117">Para exponer esta interfaz a los clientes, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ffb50-117">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="ffb50-118">Derive la clase de filtro de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="ffb50-118">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="ffb50-119">Coloque la macro [**declare \_ IUNKNOWN**](declare-iunknown.md) en la sección declaración pública.</span><span class="sxs-lookup"><span data-stu-id="ffb50-119">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="ffb50-120">Invalide [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para comprobar el IID de la interfaz y devolver un puntero al filtro.</span><span class="sxs-lookup"><span data-stu-id="ffb50-120">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="ffb50-121">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ffb50-121">The following code shows these steps:</span></span>


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



<span data-ttu-id="ffb50-122">Para obtener más información, vea [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ffb50-122">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="ffb50-123">Creación de objetos</span><span class="sxs-lookup"><span data-stu-id="ffb50-123">Object Creation</span></span>

<span data-ttu-id="ffb50-124">Si planea empaquetar el filtro en un archivo DLL y ponerlo a disposición de otros clientes, debe admitir [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y otras funciones com relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ffb50-124">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="ffb50-125">La biblioteca de clases base implementa la mayor parte de esto; solo tiene que proporcionar información sobre el filtro.</span><span class="sxs-lookup"><span data-stu-id="ffb50-125">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="ffb50-126">En esta sección se proporciona una breve descripción de lo que hay que hacer.</span><span class="sxs-lookup"><span data-stu-id="ffb50-126">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="ffb50-127">Para obtener más información, vea [Cómo crear un archivo dll de filtro de DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="ffb50-127">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="ffb50-128">En primer lugar, escriba un método de clase estática que devuelva una nueva instancia del filtro.</span><span class="sxs-lookup"><span data-stu-id="ffb50-128">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="ffb50-129">Puede asignar el nombre que desee a este método, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ffb50-129">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="ffb50-130">A continuación, declare una matriz global de instancias de la clase [**CFactoryTemplate**](cfactorytemplate.md) , denominada *g \_ templates*.</span><span class="sxs-lookup"><span data-stu-id="ffb50-130">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="ffb50-131">Cada clase **CFactoryTemplate** contiene información del registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="ffb50-131">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="ffb50-132">Varios filtros pueden residir en un único archivo DLL; simplemente incluya entradas **CFactoryTemplate** adicionales.</span><span class="sxs-lookup"><span data-stu-id="ffb50-132">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="ffb50-133">También puede declarar otros objetos COM, como páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ffb50-133">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="ffb50-134">Defina un entero global denominado *g \_ cTemplates* cuyo valor sea igual a la longitud de la matriz de *\_ plantillas g* :</span><span class="sxs-lookup"><span data-stu-id="ffb50-134">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="ffb50-135">Por último, implemente las funciones de registro de archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="ffb50-135">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="ffb50-136">En el ejemplo siguiente se muestra la implementación mínima para estas funciones:</span><span class="sxs-lookup"><span data-stu-id="ffb50-136">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="ffb50-137">Filtrar entradas del registro</span><span class="sxs-lookup"><span data-stu-id="ffb50-137">Filter Registry Entries</span></span>

<span data-ttu-id="ffb50-138">En los ejemplos anteriores se muestra cómo registrar el CLSID de un filtro para COM.</span><span class="sxs-lookup"><span data-stu-id="ffb50-138">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="ffb50-139">Para muchos filtros, esto es suficiente.</span><span class="sxs-lookup"><span data-stu-id="ffb50-139">For many filters, this is sufficient.</span></span> <span data-ttu-id="ffb50-140">A continuación, se espera que el cliente cree el filtro mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y lo agregue al gráfico de filtros mediante una llamada a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="ffb50-140">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="ffb50-141">En algunos casos, sin embargo, es posible que desee proporcionar información adicional sobre el filtro en el registro.</span><span class="sxs-lookup"><span data-stu-id="ffb50-141">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="ffb50-142">Esta información hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ffb50-142">This information does the following:</span></span>

-   <span data-ttu-id="ffb50-143">Permite a los clientes detectar el filtro mediante el [asignador de filtros](filter-mapper.md) o el [enumerador de dispositivos del sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="ffb50-143">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="ffb50-144">Permite al administrador de gráficos de filtro detectar el filtro durante la creación automática de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffb50-144">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="ffb50-145">En el ejemplo siguiente se registra el filtro del codificador RLE en la categoría compresor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ffb50-145">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="ffb50-146">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ffb50-146">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="ffb50-147">Asegúrese de leer la sección [directrices para registrar filtros](guidelines-for-registering-filters.md), que describe las prácticas recomendadas para el registro de filtros.</span><span class="sxs-lookup"><span data-stu-id="ffb50-147">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="ffb50-148">Además, no es necesario empaquetar los filtros dentro de los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="ffb50-148">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="ffb50-149">En algunos casos, puede escribir un filtro especializado que esté diseñado únicamente para una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="ffb50-149">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="ffb50-150">En ese caso, puede compilar la clase de filtro directamente en la aplicación y crearla con el `new` operador, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ffb50-150">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ffb50-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffb50-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffb50-152">Conexión inteligente</span><span class="sxs-lookup"><span data-stu-id="ffb50-152">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="ffb50-153">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ffb50-153">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="ffb50-154">Escribir filtros de transformación</span><span class="sxs-lookup"><span data-stu-id="ffb50-154">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
