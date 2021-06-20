---
description: Exponga las nuevas interfaces de un filtro a los clientes como parte de la creación de una página de propiedades de filtro para un filtro directShow personalizado.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Paso 3. Compatibilidad con QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410028"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="eb113-104">Paso 3.</span><span class="sxs-lookup"><span data-stu-id="eb113-104">Step 3.</span></span> <span data-ttu-id="eb113-105">Compatibilidad con QueryInterface</span><span class="sxs-lookup"><span data-stu-id="eb113-105">Support QueryInterface</span></span>

<span data-ttu-id="eb113-106">Para exponer las nuevas interfaces del filtro a los clientes, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb113-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="eb113-107">Incluya la [**macro DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la sección de declaración pública del filtro:</span><span class="sxs-lookup"><span data-stu-id="eb113-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="eb113-108">Invalide [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para comprobar los IID de las dos interfaces:</span><span class="sxs-lookup"><span data-stu-id="eb113-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

<span data-ttu-id="eb113-109">Siguiente: [Paso 4. Cree la página de propiedades](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="eb113-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb113-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb113-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb113-111">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="eb113-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="eb113-112">Cómo implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb113-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



