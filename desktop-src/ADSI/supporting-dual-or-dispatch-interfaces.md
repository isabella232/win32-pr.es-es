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
# <a name="supporting-dual-or-dispatch-interfaces"></a>Compatibilidad con interfaces duales o de distribución

Al igual que la interfaz de envío, todas las interfaces duales deben heredar de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), que delega todas sus funciones **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) a la **IDispatch** del agregador (ADSI). Para delegar, un objeto de extensión debe consultar el **IDispatch** del agregador, llamar al método del agregador adecuado y liberar el puntero después del uso.

Si la extensión puede ser un componente independiente, compruebe que se ha agregado. Si es así, rerute las funciones de envío a la [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del agregador; de lo contrario, puede llamar a la implementación interna de **IDispatch**, o puede llamar a la implementación de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

En el ejemplo de código siguiente se muestra cómo redirigir la llamada [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a la **IDispatch** del agregador. En este ejemplo de código se supone que la variable miembro **m \_ pOuterUnknown** se ha inicializado en el puntero **IUnknown** del agregador.


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



Se recomienda encarecidamente a los escritores de extensiones que admitan interfaces duales en lugar de las interfaces de distribución en sus objetos de extensión. Una interfaz dual permite a un cliente tener un acceso más rápido, siempre y cuando el acceso vtable esté habilitado en el cliente. Para obtener más información, vea [enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md). En función del modelo actual, la implementación de interfaces duales no debe ser más difícil que la implementación de interfaces de distribución.

 

 