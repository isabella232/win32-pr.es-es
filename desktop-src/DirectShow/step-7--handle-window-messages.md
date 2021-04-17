---
description: Paso 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Paso 7. Controlar mensajes de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678265"
---
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="feb04-104">Paso 7.</span><span class="sxs-lookup"><span data-stu-id="feb04-104">Step 7.</span></span> <span data-ttu-id="feb04-105">Controlar mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="feb04-105">Handle Window Messages</span></span>

<span data-ttu-id="feb04-106">Invalide el método [**CBasePropertyPage:: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) para actualizar los controles de cuadro de diálogo en respuesta a los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="feb04-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="feb04-107">Si no controla un mensaje determinado, llame al método **OnReceiveMessage** en la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="feb04-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="feb04-108">Siempre que el usuario cambie una propiedad, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="feb04-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="feb04-109">Establezca la variable **m \_ bDirty** de la página de propiedades en **true**.</span><span class="sxs-lookup"><span data-stu-id="feb04-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="feb04-110">Llame al método **IPropertyPageSite:: OnStatusChange** del marco de propiedades con la \_ marca de modificado PROPPAGESTATUS.</span><span class="sxs-lookup"><span data-stu-id="feb04-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="feb04-111">Esta marca informa al marco de propiedades de que debe habilitar el botón **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="feb04-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="feb04-112">El miembro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) contiene un puntero a la interfaz **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="feb04-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="feb04-113">Para simplificar este paso, puede Agregar la siguiente función auxiliar a la página de propiedades:</span><span class="sxs-lookup"><span data-stu-id="feb04-113">To simplify this step, you can add the following helper function to your property page:</span></span>


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



<span data-ttu-id="feb04-114">Llame a este método privado dentro de **OnReceiveMessage** siempre que una acción del usuario cambie una propiedad, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="feb04-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


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



<span data-ttu-id="feb04-115">La página de propiedades de este ejemplo tiene dos controles, una barra deslizante y un botón **revertir al valor predeterminado** .</span><span class="sxs-lookup"><span data-stu-id="feb04-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="feb04-116">Si el usuario desplaza la barra deslizante, la página de propiedades establece el valor de saturación en el filtro.</span><span class="sxs-lookup"><span data-stu-id="feb04-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="feb04-117">Si el usuario hace clic en el botón, la página de propiedades restaura el valor de saturación predeterminado del filtro.</span><span class="sxs-lookup"><span data-stu-id="feb04-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="feb04-118">En cada caso, m \_ lNewVal contiene el valor actual y m \_ lVal contiene el valor original.</span><span class="sxs-lookup"><span data-stu-id="feb04-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="feb04-119">El valor de m \_ lVal no se actualiza hasta que el usuario confirma el cambio, lo que sucede cuando el usuario hace clic en el botón **Aceptar** o **aplicar** en el marco de propiedades.</span><span class="sxs-lookup"><span data-stu-id="feb04-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="feb04-120">Siguiente: [paso 8. Aplicar cambios de propiedad](step-8--apply-property-changes.md).</span><span class="sxs-lookup"><span data-stu-id="feb04-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="feb04-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="feb04-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb04-122">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="feb04-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



