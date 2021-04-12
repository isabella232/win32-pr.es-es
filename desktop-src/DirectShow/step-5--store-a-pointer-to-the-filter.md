---
description: Paso 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Paso 5. Almacenar un puntero al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278287"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="5d8b5-104">Paso 5.</span><span class="sxs-lookup"><span data-stu-id="5d8b5-104">Step 5.</span></span> <span data-ttu-id="5d8b5-105">Almacenar un puntero al filtro</span><span class="sxs-lookup"><span data-stu-id="5d8b5-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="5d8b5-106">Invalide el método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) para almacenar un puntero al filtro.</span><span class="sxs-lookup"><span data-stu-id="5d8b5-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="5d8b5-107">En el ejemplo siguiente se consulta el parámetro *pUnk* de la interfaz ISaturation personalizada del filtro:</span><span class="sxs-lookup"><span data-stu-id="5d8b5-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


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



<span data-ttu-id="5d8b5-108">Siguiente: [paso 6. Inicialice el cuadro de diálogo](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="5d8b5-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d8b5-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d8b5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d8b5-110">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="5d8b5-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



