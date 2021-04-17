---
description: Paso 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Paso 8. Aplicar cambios de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678264"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="5897d-104">Paso 8.</span><span class="sxs-lookup"><span data-stu-id="5897d-104">Step 8.</span></span> <span data-ttu-id="5897d-105">Aplicar cambios de propiedad</span><span class="sxs-lookup"><span data-stu-id="5897d-105">Apply Property Changes</span></span>

<span data-ttu-id="5897d-106">Invalide el método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) para confirmar cualquier cambio de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5897d-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="5897d-107">En este ejemplo, la \_ variable m lNewVal se actualiza cada vez que el usuario se desplaza por la barra deslizante.</span><span class="sxs-lookup"><span data-stu-id="5897d-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="5897d-108">El método **OnApplyChanges** copia este valor en la \_ variable lVal de m, sobrescribiendo el valor original:</span><span class="sxs-lookup"><span data-stu-id="5897d-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="5897d-109">Siguiente: [paso 9. Desconecte la página de propiedades](step-9--disconnect-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="5897d-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5897d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5897d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5897d-111">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="5897d-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



