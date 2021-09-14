---
title: Cómo crear un control de calendario mensual
description: En este tema se muestra cómo crear dinámicamente un control de calendario mensual mediante la función CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061400"
---
# <a name="how-to-create-a-month-calendar-control"></a>Cómo crear un control de calendario mensual

En este tema se muestra cómo crear dinámicamente un control de calendario mensual mediante la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para crear un control de calendario mensual, use la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique [**MONTHCAL \_ CLASS**](common-control-window-classes.md) como clase de ventana. En primer lugar, debe registrar la clase de ventana llamando a la función [**InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) especificando el bit **DE CLASES DE \_ FECHA \_ DE JAVA** EN LA ESTRUCTURA [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que lo acompaña.

En el ejemplo siguiente se muestra cómo crear un control de calendario mensual en un cuadro de diálogo modeless existente. Tenga en cuenta que los valores de tamaño pasados [**a CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) son todos ceros. Dado que el tamaño mínimo necesario depende de la fuente que use el control, en el ejemplo se usa la macro [**\_ MonthCal GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) para solicitar información de tamaño y, a continuación, se cambia el tamaño del control mediante una llamada a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si posteriormente cambia la fuente con [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont), las dimensiones del control no cambiarán. Debe llamar de **nuevo a MonthCal \_ GetMinReqRect y** cambiar el tamaño del control para que se ajuste a la nueva fuente.



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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de calendario mensual](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Acerca de los controles de calendario mensual](month-calendar-controls.md)
</dt> <dt>

[Usar controles de calendario mensual](using-month-calendar-controls.md)
</dt> </dl>

 

 