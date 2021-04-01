---
title: Cómo crear un control de calendario mensual
description: En este tema se muestra cómo crear dinámicamente un control de calendario mensual mediante la función CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797337"
---
# <a name="how-to-create-a-month-calendar-control"></a><span data-ttu-id="93a92-103">Cómo crear un control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="93a92-103">How to Create a Month Calendar Control</span></span>

<span data-ttu-id="93a92-104">En este tema se muestra cómo crear dinámicamente un control de calendario mensual mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="93a92-104">This topic demonstrates how to dynamically create a month calendar control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="93a92-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="93a92-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="93a92-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="93a92-106">Technologies</span></span>

-   [<span data-ttu-id="93a92-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="93a92-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="93a92-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="93a92-108">Prerequisites</span></span>

-   <span data-ttu-id="93a92-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="93a92-109">C/C++</span></span>
-   <span data-ttu-id="93a92-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="93a92-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="93a92-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="93a92-111">Instructions</span></span>


<span data-ttu-id="93a92-112">Para crear un control de calendario mensual, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique [**la \_ clase MONTHCAL**](common-control-window-classes.md) como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="93a92-112">To create a month calendar control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**MONTHCAL\_CLASS**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="93a92-113">Primero debe registrar la clase de ventana mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando el bit de **\_ \_ las clases de fecha de ICC** en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="93a92-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the **ICC\_DATE\_CLASSES** bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="93a92-114">En el ejemplo siguiente se muestra cómo crear un control de calendario mensual en un cuadro de diálogo no modal existente.</span><span class="sxs-lookup"><span data-stu-id="93a92-114">The following example demonstrates how to create a month calendar control in an existing modeless dialog box.</span></span> <span data-ttu-id="93a92-115">Tenga en cuenta que los valores de tamaño pasados a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) son ceros.</span><span class="sxs-lookup"><span data-stu-id="93a92-115">Note that the size values passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) are all zeros.</span></span> <span data-ttu-id="93a92-116">Dado que el tamaño mínimo necesario depende de la fuente que utiliza el control, en el ejemplo se usa la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) para solicitar información de tamaño y, a continuación, se cambia el tamaño del control llamando a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="93a92-116">Because the minimum required size depends on the font that the control uses, the example uses the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro to request size information and then resizes the control by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="93a92-117">Si posteriormente cambia la fuente con [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont), las dimensiones del control no cambiarán.</span><span class="sxs-lookup"><span data-stu-id="93a92-117">If you subsequently change the font with [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont), the dimensions of the control will not change.</span></span> <span data-ttu-id="93a92-118">Debe llamar de nuevo a **MonthCal \_ GetMinReqRect** y cambiar el tamaño del control para que se ajuste a la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="93a92-118">You must call **MonthCal\_GetMinReqRect** again and resize the control to fit the new font.</span></span>



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="93a92-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93a92-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93a92-120">Referencia de control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="93a92-120">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="93a92-121">Acerca de los controles de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="93a92-121">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="93a92-122">Usar controles de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="93a92-122">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 