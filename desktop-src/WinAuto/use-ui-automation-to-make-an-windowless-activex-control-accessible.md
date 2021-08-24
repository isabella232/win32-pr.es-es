---
title: Cómo usar Automatización de la interfaz de usuario para que un control de ActiveX sin ventanas sea accesible
description: Describe cómo usar Microsoft Automatización de la interfaz de usuario \ 32; API para asegurarse de que las aplicaciones cliente de tecnología de asistencia (AT) pueden acceder al control de ActiveX sin ventanas de Microsoft.
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Control de ActiveX sin ventanas, accesibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570365"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>Cómo usar Automatización de la interfaz de usuario para que un control de ActiveX sin ventanas sea accesible

Describe cómo usar microsoft Automatización de la interfaz de usuario API para asegurarse de que el control de ActiveX de Microsoft sin ventanas es accesible para las aplicaciones cliente de tecnología de asistencia (AT).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Automatización de la interfaz de usuario](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Programación de Microsoft Win32 y Component Object Model (COM)
-   Controles de ActiveX sin ventanas
-   Automatización de la interfaz de usuario proveedores

## <a name="instructions"></a>Instructions

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Paso 1: Implementar las interfaces Automatización de la interfaz de usuario proveedor de recursos.

Para que la aplicación sea accesible, debe implementar las interfaces del proveedor de Automatización de la interfaz de usuario para el control ActiveX sin ventanas, [**incluidos IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) [**IRawElementProviderFragment,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)e [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). Debe implementar estas interfaces como lo haría para un control basado en ventanas, excepto como se describe en los pasos siguientes. Para obtener más información sobre la implementación de interfaces de proveedor de UIA, vea Automatización de la interfaz de usuario Guía del programador [del proveedor de aplicaciones](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Paso 2: Implementar la interfaz IServiceProvider.

Cuando un cliente necesita información de accesibilidad sobre el control sin ventanas, el contenedor de controles llama al método **IServiceProvider::QueryService** del control para recuperar el puntero de interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del control.

En el ejemplo siguiente se muestra cómo implementar el **método QueryService.**


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Paso 3: Implementar el método IRawElementProviderFragment::Navigate.

Cuando se llama al método [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) del control sin ventana para navegar al proveedor raíz del control sin ventana o al mismo nivel, el método **Navigate** debe delegar en el método [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) del contenedor de controles.

En el ejemplo siguiente se muestra cómo implementar el [**método Navigate.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Paso 4: Implementar el método IRawElementProviderFragment::GetRuntimeId.

Cuando el control sin ventana recibe una llamada a su método [**IRawElementProviderFragment::GetRuntimeId,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) el control debe hacer lo siguiente:

1.  Recupere un prefijo de identificador de tiempo de ejecución llamando al método [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix del**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) sitio de control.
2.  Cree un identificador de tiempo de ejecución único para el control anexando un entero al prefijo de identificador de tiempo de ejecución.
3.  Devuelve el identificador de tiempo de ejecución al autor de la llamada.

En el ejemplo siguiente se muestra cómo implementar el [**método GetRuntimeId.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix)


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MSAA para hacer que un control de ActiveX sin ventanas sea accesible](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accesibilidad del control ActiveX sin ventanas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 