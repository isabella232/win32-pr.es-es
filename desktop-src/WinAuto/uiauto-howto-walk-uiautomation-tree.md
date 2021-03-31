---
title: Cómo recorrer el árbol de automatización de la interfaz de usuario
description: Este tema contiene código de ejemplo que muestra cómo usar la interfaz IUIAutomationTreeWalker para recorrer y examinar los elementos del árbol de automatización de la interfaz de usuario de Microsoft.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903398"
---
# <a name="how-to-walk-the-ui-automation-tree"></a><span data-ttu-id="0e267-103">Cómo recorrer el árbol de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0e267-103">How to Walk the UI Automation Tree</span></span>

<span data-ttu-id="0e267-104">Este tema contiene código de ejemplo que muestra cómo usar la interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para recorrer y examinar los elementos del árbol de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0e267-104">This topic contains example code that shows how to use the [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface to walk through and examine the elements in the Microsoft UI Automation tree.</span></span> <span data-ttu-id="0e267-105">Se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0e267-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="0e267-106">Recorrer los descendientes de un elemento</span><span class="sxs-lookup"><span data-stu-id="0e267-106">Walking through Descendants of an Element</span></span>](#walking-through-descendants-of-an-element)
-   [<span data-ttu-id="0e267-107">Recorrer elementos antecesores</span><span class="sxs-lookup"><span data-stu-id="0e267-107">Walking through Ancestor Elements</span></span>](#walking-through-ancestor-elements)
-   [<span data-ttu-id="0e267-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e267-108">Related topics</span></span>](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a><span data-ttu-id="0e267-109">Recorrer los descendientes de un elemento</span><span class="sxs-lookup"><span data-stu-id="0e267-109">Walking through Descendants of an Element</span></span>

<span data-ttu-id="0e267-110">El siguiente ejemplo de código es una función recursiva que recorre todos los descendientes de un elemento de la interfaz de usuario y muestra sus tipos de control en una lista jerárquica.</span><span class="sxs-lookup"><span data-stu-id="0e267-110">The following code example is a recursive function that walks through all the descendants of a UI element and displays their control types in a hierarchical list.</span></span>


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a><span data-ttu-id="0e267-111">Recorrer elementos antecesores</span><span class="sxs-lookup"><span data-stu-id="0e267-111">Walking through Ancestor Elements</span></span>

<span data-ttu-id="0e267-112">El siguiente ejemplo de código es una función que le guía a través de los antecesores de un elemento para identificar el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="0e267-112">The following code example is a function that walks through the ancestors of a element to identify the parent element.</span></span> <span data-ttu-id="0e267-113">Esto resulta útil cuando es necesario identificar la ventana primaria de un control.</span><span class="sxs-lookup"><span data-stu-id="0e267-113">This is useful when you need to identify the parent window of a control.</span></span> <span data-ttu-id="0e267-114">La función devuelve **null** para los elementos de nivel superior; es decir, los elementos cuyo elemento primario es el escritorio.</span><span class="sxs-lookup"><span data-stu-id="0e267-114">The function returns **NULL** for top-level elements; that is, elements whose parent is the desktop.</span></span>


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a><span data-ttu-id="0e267-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e267-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0e267-116">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0e267-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e267-117">Obtener elementos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="0e267-117">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="0e267-118">Temas de procedimientos para clientes de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0e267-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




