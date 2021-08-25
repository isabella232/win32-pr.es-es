---
title: Cómo crear un control List-View control
description: En este tema se muestra cómo crear un control list-view. Para crear un control list-view, use las funciones CreateWindow o CreateWindowEx y especifique la clase \_ de ventana WC LISTVIEW.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826615"
---
# <a name="how-to-create-a-list-view-control"></a>Cómo crear un control List-View control

En este tema se muestra cómo crear un control list-view. Para crear un control list-view, use las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la [**clase de ventana WC \_ LISTVIEW.**](common-control-window-classes.md)

También se puede crear un control de vista de lista como parte de una plantilla de cuadro de diálogo. Debe especificar [**WC \_ LISTVIEW como**](common-control-window-classes.md) nombre de clase. Para usar un control de vista de lista como parte de una plantilla de cuadro de diálogo, debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) antes de crear una instancia del cuadro de diálogo.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


En primer lugar, registre la clase de ventana llamando a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y especificando el bit [**CLASS DE \_ \_ LISTVIEW DE LA CLASE DE INSTRUCCIÓN**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) EN LA ESTRUCTURA **INITCOMMONCONTROLSEX** que lo acompaña. Esto garantiza que se cargue el archivo DLL de controles comunes. A continuación, use [**las funciones CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) [**o CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la [**clase de ventana WC \_ LISTVIEW.**](common-control-window-classes.md)

> [!Note]  
> De forma predeterminada, un control de vista de lista usa la fuente de título del icono. Sin embargo, puede usar un mensaje [**\_ WM SETFONT**](/windows/desktop/winmsg/wm-setfont) para especificar la fuente que se usará para el texto. Debe enviar este mensaje antes de insertar los elementos. El control usa las dimensiones de la fuente especificadas por el mensaje **\_ WM SETFONT** para determinar el espaciado y el diseño. También puede personalizar la fuente de cada elemento. Para obtener más información, vea [Custom Draw](custom-draw.md).

 

En el siguiente ejemplo de código de C++ se crea un control list-view en la vista de informe.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




Normalmente, las aplicaciones de vista de lista permiten al usuario cambiar de una vista a otra.

En el siguiente ejemplo de código de C++ se cambia el estilo de ventana de la vista de lista, que a su vez cambia la vista.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del control List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 