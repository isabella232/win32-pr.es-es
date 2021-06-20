---
description: Implemente la interfaz ISpecifyPropertyPages en el filtro como parte de la creación de una página de propiedades de filtro para un filtro directShow personalizado.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Paso 2. Implementación de ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410058"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="8bce7-104">Paso 2.</span><span class="sxs-lookup"><span data-stu-id="8bce7-104">Step 2.</span></span> <span data-ttu-id="8bce7-105">Implementación de ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="8bce7-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="8bce7-106">A continuación, **implemente la interfaz ISpecifyPropertyPages** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="8bce7-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="8bce7-107">Esta interfaz tiene un único método, **GetPages**, que devuelve una matriz de CLID para las páginas de propiedades que admite el filtro.</span><span class="sxs-lookup"><span data-stu-id="8bce7-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="8bce7-108">En este ejemplo, el filtro tiene una sola página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8bce7-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="8bce7-109">Empiece por generar el CLSID y declararlo en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8bce7-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="8bce7-110">Ahora implemente **el método GetPages:**</span><span class="sxs-lookup"><span data-stu-id="8bce7-110">Now implement the **GetPages** method:</span></span>


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



<span data-ttu-id="8bce7-111">Asigne memoria para la matriz **mediante CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="8bce7-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="8bce7-112">El autor de la llamada liberará la memoria.</span><span class="sxs-lookup"><span data-stu-id="8bce7-112">The caller will release the memory.</span></span>

<span data-ttu-id="8bce7-113">Siguiente: [Paso 3. Compatibilidad con QueryInterface](step-3--support-queryinterface.md).</span><span class="sxs-lookup"><span data-stu-id="8bce7-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bce7-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bce7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bce7-115">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="8bce7-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



