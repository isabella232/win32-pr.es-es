---
title: Cómo habilitar la navegación en un proveedor Automatización de la interfaz de usuario fragmentos
description: Este tema contiene código de ejemplo que muestra cómo habilitar la navegación en un proveedor de Automatización de la interfaz de usuario Microsoft para un elemento de un fragmento.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070512"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Cómo habilitar la navegación en un proveedor Automatización de la interfaz de usuario fragmentos

Este tema contiene código de ejemplo que muestra cómo habilitar la navegación en un proveedor de Automatización de la interfaz de usuario Microsoft para un elemento de un fragmento.

El código de ejemplo siguiente implementa el [**método IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) para un elemento de lista en un control de lista personalizado. El elemento primario es el control de lista personalizado y los elementos relacionados son otros elementos de la lista. El método establece el *parámetro pRetVal* en **NULL** si no hay ningún elemento en la dirección especificada.


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de un proveedor Server-Side Automatización de la interfaz de usuario aplicación](uiauto-serversideprovider.md)
</dt> <dt>

[Temas de ayuda para proveedores de Automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




