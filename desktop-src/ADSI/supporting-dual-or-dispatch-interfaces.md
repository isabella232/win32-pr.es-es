---
title: Compatibilidad con interfaces duales o de distribución
description: Al igual que la interfaz de distribución, todas las interfaces duales deben heredar de IDispatch, que delega todas sus funciones IDispatch (GetIDsOfNames, Invoke, GetTypeInfo y GetTypeInfoCount) de nuevo en el IDispatch del agregador (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Compatibilidad con interfaces duales o de distribución ADSI
- extensiones ADSI, interfaces duales o de distribución
- ADSI ADSI , código de ejemplo C/C++, delegación de métodos IDispatch al agregador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172106"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>Compatibilidad con interfaces duales o de distribución

Al igual que la interfaz de distribución, todas las interfaces duales deben heredar de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), que delega todas sus funciones **IDispatch** [**(GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo)y [**GetTypeInfoCount)**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)de nuevo en **el IDispatch** del agregador (ADSI). Para delegar, un objeto de extensión debe consultar el **IDispatch** del agregador, llamar al método de agregador adecuado y liberar el puntero después de su uso.

Si la extensión puede ser un componente independiente, compruebe que está agregada. Si es así, vuelva a enrutar las funciones de distribución a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del agregador; de lo contrario, puede llamar a la implementación interna de **IDispatch** o puede llamar a la implementación de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

En el ejemplo de código siguiente se muestra cómo volver a enrutar la llamada [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) al **IDispatch** del agregador. En este ejemplo de código se supone que la variable miembro **\_ m pOuterUnknown** se ha inicializado en el **puntero IUnknown** del agregador.


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



Se recomienda encarecidamente a los escritores de extensiones que admitan interfaces duales en lugar de interfaces de distribución en sus objetos de extensión. Una interfaz dual permite a un cliente tener un acceso más rápido, siempre y cuando el acceso de vtable esté habilitado en el cliente. Para obtener más información, vea [Enlace en tiempo de tarde frente al acceso de Vtable en el modelo de extensión ADSI.](late-binding-vs--vtable-access-in-the-adsi-extension-model.md) En función del modelo actual, la implementación de interfaces duales no debe ser más difícil que implementar interfaces de distribución.

 

 