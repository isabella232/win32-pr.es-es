---
description: Paso 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Paso 9. Desconectar la página de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688219"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="99374-104">Paso 9.</span><span class="sxs-lookup"><span data-stu-id="99374-104">Step 9.</span></span> <span data-ttu-id="99374-105">Desconectar la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="99374-105">Disconnect the Property Page</span></span>

<span data-ttu-id="99374-106">Invalide el método [**CBasePropertyPage:: OnDisconnection**](cbasepropertypage-ondisconnect.md) para liberar las interfaces que haya obtenido en el método **alconnect** .</span><span class="sxs-lookup"><span data-stu-id="99374-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="99374-107">Además, si el usuario descarta la hoja de propiedades sin confirmar los cambios, debe restaurar los valores originales si han cambiado.</span><span class="sxs-lookup"><span data-stu-id="99374-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="99374-108">No hay ningún método "OnCancel" al que se llama cuando el usuario cancela, por lo que necesita realizar un seguimiento de si el usuario ha llamado a **OnApplyChanges**.</span><span class="sxs-lookup"><span data-stu-id="99374-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="99374-109">En este ejemplo se utiliza la \_ variable m lVal, descrita anteriormente:</span><span class="sxs-lookup"><span data-stu-id="99374-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="99374-110">Siguiente: [paso 10. Compatibilidad con el registro COM](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="99374-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="99374-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99374-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99374-112">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="99374-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



