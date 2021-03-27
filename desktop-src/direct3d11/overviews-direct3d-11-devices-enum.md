---
title: Cómo enumerar adaptadores
description: En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para enumerar los adaptadores de gráficos disponibles en un equipo.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997108"
---
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="44e17-103">Cómo: enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="44e17-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="44e17-104">En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para enumerar los adaptadores de gráficos disponibles en un equipo.</span><span class="sxs-lookup"><span data-stu-id="44e17-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="44e17-105">Direct3D 10 y 11 pueden usar DXGI para enumerar los adaptadores.</span><span class="sxs-lookup"><span data-stu-id="44e17-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="44e17-106">Por lo general, es necesario enumerar los adaptadores por estos motivos:</span><span class="sxs-lookup"><span data-stu-id="44e17-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="44e17-107">Para determinar el número de adaptadores de gráficos instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="44e17-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="44e17-108">Para ayudarle a elegir el adaptador que se va a usar para crear un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="44e17-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="44e17-109">Para recuperar un objeto [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) que puede usar para recuperar funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44e17-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="44e17-110">**Para enumerar adaptadores**</span><span class="sxs-lookup"><span data-stu-id="44e17-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="44e17-111">Cree un objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) mediante una llamada a la función [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="44e17-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="44e17-112">En el ejemplo de código siguiente se muestra cómo inicializar un objeto **IDXGIFactory** .</span><span class="sxs-lookup"><span data-stu-id="44e17-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="44e17-113">Enumere cada adaptador llamando al método [**IDXGIFactory:: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) .</span><span class="sxs-lookup"><span data-stu-id="44e17-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="44e17-114">El parámetro *Adapter* permite especificar un número de índice de base cero del adaptador que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="44e17-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="44e17-115">Si no hay ningún adaptador disponible en el índice especificado, el método devuelve el [**error de DXGI \_ \_ no \_ encontrado**](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="44e17-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="44e17-116">En el ejemplo de código siguiente se muestra cómo enumerar a través de los adaptadores de un equipo.</span><span class="sxs-lookup"><span data-stu-id="44e17-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="44e17-117">En el ejemplo de código siguiente se muestra cómo enumerar todos los adaptadores de un equipo.</span><span class="sxs-lookup"><span data-stu-id="44e17-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="44e17-118">En Direct3D 11,0 y versiones posteriores, se recomienda que las aplicaciones siempre usen [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) y [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="44e17-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a><span data-ttu-id="44e17-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44e17-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44e17-120">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="44e17-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 