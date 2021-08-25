---
description: Invalide el método CBasePropertyPage::OnActivate para inicializar el cuadro de diálogo como parte de la creación de una página de propiedades de filtro para un filtro DirectShow personalizado.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Paso 6. Inicializar el cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2ac2dbc4e8ed59317db3db46079b087e4afcf0fa8dce315aa2a0cbd45d502a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102315"
---
# <a name="step-6-initialize-the-dialog"></a>Paso 6. Inicializar el cuadro de diálogo

Invalide [**el método CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) para inicializar el cuadro de diálogo. En este ejemplo, la página de propiedades usa un control deslizante, por lo que el primer paso de **OnActivate** es inicializar la biblioteca de controles común. A continuación, el método inicializa el control deslizante con el valor actual de la propiedad de saturación del filtro:


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



Siguiente: [Paso 7. Controlar mensajes de ventana](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



