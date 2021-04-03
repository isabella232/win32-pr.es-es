---
title: Cómo habilitar la navegación en un proveedor de fragmentos de UI Automation
description: Este tema contiene código de ejemplo que muestra cómo habilitar la navegación en un proveedor de automatización de la interfaz de usuario de Microsoft para un elemento de un fragmento.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075197"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Cómo habilitar la navegación en un proveedor de fragmentos de UI Automation

Este tema contiene código de ejemplo que muestra cómo habilitar la navegación en un proveedor de automatización de la interfaz de usuario de Microsoft para un elemento de un fragmento.

En el ejemplo de código siguiente se implementa el método [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) para un elemento de lista de un control de lista personalizado. El elemento primario es el control de lista personalizado y los elementos del mismo nivel son otros elementos de la lista. El método establece el parámetro *pRetVal* en **null** si no hay ningún elemento en la dirección especificada.


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

**Vista**
</dt> <dt>

[Implementar un proveedor de automatización de la interfaz de usuario de Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Temas de procedimientos para los proveedores de automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




