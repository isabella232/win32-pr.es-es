---
title: Hospedar un Automatización de la interfaz de usuario control de ActiveX sin ventanas
description: Obtenga información sobre cómo crear un contenedor de controles que pueda hospedar controles de Microsoft ActiveX sin ventanas que implementen Microsoft Automatización de la interfaz de usuario.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Automatización de la interfaz de usuario, control de ActiveX sin ActiveX ventana
- Control de ActiveX sin ventanas, Automatización de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568533"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>Hospedar un Automatización de la interfaz de usuario control de ActiveX sin ventanas

Obtenga información sobre cómo crear un contenedor de controles que pueda hospedar controles de Microsoft ActiveX sin ventanas que implementen Microsoft Automatización de la interfaz de usuario. Mediante los pasos descritos aquí, puede asegurarse de que las aplicaciones cliente de tecnología de asistencia (AT) pueden acceder Automatización de la interfaz de usuario los controles sin ventanas que se hospedan en el contenedor de controles.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Automatización de la interfaz de usuario](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de Microsoft Win32 y modelo de objetos componentes (COM)
-   Controles de ActiveX sin ventanas
-   Automatización de la interfaz de usuario proveedores

## <a name="instructions"></a>Instructions

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>Paso 1: Proporcione la interfaz IRawElementProviderSimple en nombre del control sin ventanas.

Siempre que el sistema necesite [**el puntero IRawElementProviderSimple para**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) la raíz de un control sin ventanas, el sistema consulta el contenedor de controles. Para recuperar el puntero, el contenedor llama a la implementación del control sin ventanas del [**método IServiceProvider::QueryService.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))

Si el contenedor de controles tiene Automatización de la interfaz de usuario implementación, puede devolver el puntero [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del control sin ventanas al sistema.

Si el contenedor de controles tiene una implementación de Microsoft Active Accessibility, llame a la función [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) para obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que represente el control y, a continuación, devuelva el puntero de interfaz **IAccessible** al sistema.

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>Paso 2: Implementar la interfaz IRawElementProviderWindowlessSite.

Un contenedor de controles implementa la [**interfaz IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) para habilitar un control sin ventanas basado en Automatización de la interfaz de usuario para comunicar su información de accesibilidad.

1.  Implemente [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).

    Un fragmento de control sin ventanas debe crear un identificador de tiempo de ejecución único para sí mismo. Para crear su identificador de tiempo de ejecución, un fragmento de control sin ventanas recupera un valor de prefijo llamando al método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sitio de control y, a continuación, anexa al prefijo un valor entero que es único con respecto a todos los demás fragmentos del control sin ventanas.

    El sitio de control de un control sin ventanas debe implementar el método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) mediante la formación de **una SAFEARRAY** que contenga la constante **UiaAppendRuntimeId**, seguida de un valor entero que sea único para el sitio.

    En este ejemplo se muestra cómo devolver un prefijo de identificador de tiempo de ejecución para un control sin ventanas.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  Implemente [**el método IRawElementProviderWindowlessSite::GetAdjacentFragment.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment)

    Un control que implementa Automatización de la interfaz de usuario debe devolver un puntero al proveedor de fragmentos primario del control.

    Para devolver el elemento primario del fragmento, un objeto que implementa la interfaz [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) debe poder implementar el [**método Navigate.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) Implementar **Navigate es** difícil para un control sin ventanas porque es posible que el control no pueda determinar su ubicación en el árbol accesible del objeto primario. El [**método IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) permite que el control sin ventanas consulte su sitio para el fragmento adyacente y, a continuación, devuelva ese fragmento al cliente que llamó **a Navigate**.

    En este ejemplo se muestra cómo un contenedor de controles recupera el fragmento primario de un control sin ventanas.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>Paso 3: Opcional: Implemente la interfaz IRawElementProviderHostingAccessibles.

Implemente la [**interfaz IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) si el contenedor de controles tiene una implementación de proveedor de Automatización de la interfaz de usuario que es la raíz de un árbol de accesibilidad que incluye controles ActiveX sin ventanas que admiten Microsoft Active Accessibility. La **interfaz IRawElementProviderHostingAccessibles** tiene un único método, [**GetEmbeddedAccessibles,**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles)que recupera los punteros de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de todos los controles ActiveX sin ventanas basados en Microsoft Active Accessibility hospedados por el contenedor de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo hospedar un control de ActiveX sin ventanas de MSAA](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[Accesibilidad de ActiveX control sin ventanas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 