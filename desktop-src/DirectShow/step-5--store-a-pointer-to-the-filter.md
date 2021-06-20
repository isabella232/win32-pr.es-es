---
description: Almacene un puntero a un filtro como parte de la creación de una página de propiedades de filtro para un filtro directShow personalizado.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Paso 5. Almacenar un puntero al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406798"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="f5af9-104">Paso 5.</span><span class="sxs-lookup"><span data-stu-id="f5af9-104">Step 5.</span></span> <span data-ttu-id="f5af9-105">Almacenar un puntero al filtro</span><span class="sxs-lookup"><span data-stu-id="f5af9-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="f5af9-106">Invalide [**el método CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) para almacenar un puntero al filtro.</span><span class="sxs-lookup"><span data-stu-id="f5af9-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="f5af9-107">En el ejemplo siguiente se consulta *el parámetro pUnk* para la interfaz de ISaturation personalizada del filtro:</span><span class="sxs-lookup"><span data-stu-id="f5af9-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



<span data-ttu-id="f5af9-108">Siguiente: [Paso 6. Inicialice el cuadro de diálogo](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="f5af9-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5af9-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5af9-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5af9-110">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="f5af9-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



