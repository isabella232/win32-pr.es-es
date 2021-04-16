---
title: Compatibilidad con interfaces duales o de distribución
description: Al igual que la interfaz de envío, todas las interfaces duales deben heredar de IDispatch, que delega todas sus funciones IDispatch (GetIDsOfNames, Invoke, GetTypeInfo, GetTypeInfoCount) a la IDispatch del agregador (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Compatibilidad con las interfaces dual o de distribución ADSI
- extensiones ADSI, dual o de distribución
- ADSI ADSI, código de ejemplo C/C++, Delegación de métodos IDispatch al agregador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656405"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a><span data-ttu-id="67bf3-106">Compatibilidad con interfaces duales o de distribución</span><span class="sxs-lookup"><span data-stu-id="67bf3-106">Supporting Dual or Dispatch Interfaces</span></span>

<span data-ttu-id="67bf3-107">Al igual que la interfaz de envío, todas las interfaces duales deben heredar de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), que delega todas sus funciones **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) a la **IDispatch** del agregador (ADSI).</span><span class="sxs-lookup"><span data-stu-id="67bf3-107">Like the dispatch interface, all dual interfaces must inherit from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), which delegates all of its **IDispatch** functions ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) back to the **IDispatch** of the aggregator (ADSI).</span></span> <span data-ttu-id="67bf3-108">Para delegar, un objeto de extensión debe consultar el **IDispatch** del agregador, llamar al método del agregador adecuado y liberar el puntero después del uso.</span><span class="sxs-lookup"><span data-stu-id="67bf3-108">In order to delegate, an extension object should query for the **IDispatch** of the aggregator, call the appropriate aggregator method, and release the pointer after use.</span></span>

<span data-ttu-id="67bf3-109">Si la extensión puede ser un componente independiente, compruebe que se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="67bf3-109">If the extension can be a standalone component, verify that it is aggregated.</span></span> <span data-ttu-id="67bf3-110">Si es así, rerute las funciones de envío a la [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del agregador; de lo contrario, puede llamar a la implementación interna de **IDispatch**, o puede llamar a la implementación de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="67bf3-110">If so, reroute the dispatch functions to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) of the aggregator, otherwise you can call your internal implementation of **IDispatch**, or you can call your implementation of [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

<span data-ttu-id="67bf3-111">En el ejemplo de código siguiente se muestra cómo redirigir la llamada [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a la **IDispatch** del agregador.</span><span class="sxs-lookup"><span data-stu-id="67bf3-111">The following code example shows how to reroute the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) call to the **IDispatch** of the aggregator.</span></span> <span data-ttu-id="67bf3-112">En este ejemplo de código se supone que la variable miembro **m \_ pOuterUnknown** se ha inicializado en el puntero **IUnknown** del agregador.</span><span class="sxs-lookup"><span data-stu-id="67bf3-112">This code example assumes that the **m\_pOuterUnknown** member variable has been initialized to the **IUnknown** pointer of the aggregator.</span></span>


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



<span data-ttu-id="67bf3-113">Se recomienda encarecidamente a los escritores de extensiones que admitan interfaces duales en lugar de las interfaces de distribución en sus objetos de extensión.</span><span class="sxs-lookup"><span data-stu-id="67bf3-113">Extension writers are strongly encouraged to support dual interfaces instead of dispatch interfaces in their extension objects.</span></span> <span data-ttu-id="67bf3-114">Una interfaz dual permite a un cliente tener un acceso más rápido, siempre y cuando el acceso vtable esté habilitado en el cliente.</span><span class="sxs-lookup"><span data-stu-id="67bf3-114">A dual interface enables a client to have faster access, as long as vtable access is enabled in the client.</span></span> <span data-ttu-id="67bf3-115">Para obtener más información, vea [enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span><span class="sxs-lookup"><span data-stu-id="67bf3-115">For more information, see [Late Binding vs. Vtable Access in the ADSI Extension Model](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span></span> <span data-ttu-id="67bf3-116">En función del modelo actual, la implementación de interfaces duales no debe ser más difícil que la implementación de interfaces de distribución.</span><span class="sxs-lookup"><span data-stu-id="67bf3-116">Based on the current model, implementing dual interfaces should not be more difficult than implementing dispatch interfaces.</span></span>

 

 