---
description: Invalide el método CBasePropertyPage::OnActivate para inicializar el cuadro de diálogo como parte de la creación de una página de propiedades de filtro para un filtro directShow personalizado.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Paso 6. Inicializar el cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbdf18e272ac548227626bc9da4f992786a4ab3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404498"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="1cea1-104">Paso 6.</span><span class="sxs-lookup"><span data-stu-id="1cea1-104">Step 6.</span></span> <span data-ttu-id="1cea1-105">Inicializar el cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="1cea1-105">Initialize the Dialog</span></span>

<span data-ttu-id="1cea1-106">Invalide [**el método CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) para inicializar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1cea1-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="1cea1-107">En este ejemplo, la página de propiedades usa un control deslizante, por lo que el primer paso de **OnActivate** es inicializar la biblioteca de controles común.</span><span class="sxs-lookup"><span data-stu-id="1cea1-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="1cea1-108">A continuación, el método inicializa el control deslizante con el valor actual de la propiedad de saturación del filtro:</span><span class="sxs-lookup"><span data-stu-id="1cea1-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



<span data-ttu-id="1cea1-109">Siguiente: [Paso 7. Controlar mensajes de ventana](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="1cea1-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cea1-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cea1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cea1-111">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="1cea1-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



