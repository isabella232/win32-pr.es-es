---
description: Paso 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Paso 7. Controlar mensajes de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f1aa28e891dfce8715984f505d6177c75ba6dc21ed8290c6e2bebee2e8203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102305"
---
# <a name="step-7-handle-window-messages"></a>Paso 7. Controlar mensajes de ventana

Invalide [**el método CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) para actualizar los controles de diálogo en respuesta a la entrada del usuario. Si no controla un mensaje determinado, llame al **método OnReceiveMessage** en la clase primaria. Cada vez que el usuario cambie una propiedad, haga lo siguiente:

-   Establezca la **variable m \_ bDirty** de la página de propiedades en **TRUE.**
-   Llame al **método IPropertyPageSite::OnStatusChange** del marco de propiedades con la marca PROPPAGESTATUS \_ DIRTY. Esta marca informa al marco de propiedades de que debe habilitar el **botón** Aplicar. El [**miembro CBasePropertyPage::m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) contiene un puntero a la **interfaz IPropertyPageSite.**

Para simplificar este paso, puede agregar la siguiente función auxiliar a la página de propiedades:


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



Llame a este método privado **dentro de OnReceiveMessage** cada vez que una acción del usuario cambie una propiedad, como se muestra en el ejemplo siguiente:


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



La página de propiedades de este ejemplo tiene dos controles, una barra deslizante y un **botón Revertir** al valor predeterminado. Si el usuario desplaza la barra deslizante, la página de propiedades establece el valor de saturación en el filtro. Si el usuario hace clic en el botón, la página de propiedades restaura el valor de saturación predeterminado del filtro. En cada caso, m \_ lNewVal contiene el valor actual y m \_ lVal contiene el valor original. El valor de m lVal no se actualiza hasta que el usuario confirma el cambio, lo que sucede cuando el usuario hace clic en el botón Aceptar o Aplicar en el \_ marco de propiedades.  

Siguiente: [Paso 8. Aplicar cambios de propiedad](step-8--apply-property-changes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



