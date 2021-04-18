---
description: Paso 6.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Paso 6. Inicializar el cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282eb03db38c543678fb2c4ef1155e1150b419bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688220"
---
# <a name="step-6-initialize-the-dialog"></a>Paso 6. Inicializar el cuadro de diálogo

Invalide el método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) para inicializar el cuadro de diálogo. En este ejemplo, la página de propiedades usa un control deslizante, por lo que el primer paso en **OnActivate** es inicializar la biblioteca de controles comunes. Después, el método inicializa el control deslizante mediante el valor actual de la propiedad de saturación del filtro:


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



Siguiente: [paso 7. Controlar mensajes de ventana](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



