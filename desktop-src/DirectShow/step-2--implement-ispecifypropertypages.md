---
description: Paso 2.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Paso 2. Implementar ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688084"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="1b11c-104">Paso 2.</span><span class="sxs-lookup"><span data-stu-id="1b11c-104">Step 2.</span></span> <span data-ttu-id="1b11c-105">Implementar ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="1b11c-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="1b11c-106">A continuación, implemente la interfaz **ISpecifyPropertyPages** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="1b11c-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="1b11c-107">Esta interfaz tiene un método único, **GetPages**, que devuelve una matriz de CLSID para las páginas de propiedades que admite el filtro.</span><span class="sxs-lookup"><span data-stu-id="1b11c-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="1b11c-108">En este ejemplo, el filtro tiene una sola página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1b11c-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="1b11c-109">Empiece generando el CLSID y declarándolo en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1b11c-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="1b11c-110">Ahora implemente el método **GetPages** :</span><span class="sxs-lookup"><span data-stu-id="1b11c-110">Now implement the **GetPages** method:</span></span>


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



<span data-ttu-id="1b11c-111">Asigne memoria para la matriz mediante **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="1b11c-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="1b11c-112">El autor de la llamada liberará la memoria.</span><span class="sxs-lookup"><span data-stu-id="1b11c-112">The caller will release the memory.</span></span>

<span data-ttu-id="1b11c-113">Siguiente: [paso 3. Compatibilidad con QueryInterface](step-3--support-queryinterface.md).</span><span class="sxs-lookup"><span data-stu-id="1b11c-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b11c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b11c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b11c-115">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="1b11c-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



