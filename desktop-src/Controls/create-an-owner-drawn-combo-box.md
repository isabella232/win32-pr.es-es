---
title: Cómo crear un cuadro combinado Owner-Drawn base de datos
description: En este tema se muestra cómo usar un cuadro combinado dibujado por el propietario.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062220"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Cómo crear un cuadro combinado Owner-Drawn base de datos

En este tema se muestra cómo usar un cuadro combinado dibujado por el propietario. En el ejemplo de código de C++ se usa un cuadro de lista desplegable dibujado por el propietario para mostrar los cuatro grupos de alimentos, cada uno representado por un mapa de bits y un nombre. La selección de un grupo de alimentos hace que los alimentos de ese grupo aparezcan en una lista.

![captura de pantalla que muestra un cuadro de diálogo con un cuadro de lista y un cuadro de lista desplegable expandido que muestra un icono y una etiqueta para cada elemento](images/cscbx-01.png)

El cuadro de diálogo también contiene un cuadro de lista (IDLIST) y dos botones: **Aceptar** (IDOK) y **Cancelar** (IDCANCEL). Las constantes IDOK e IDCANCEL se definen mediante los archivos de encabezado del SDK. La constante IDLIST se define en el archivo de encabezado de la aplicación, al igual que el identificador de control, IDCOMBO. Para obtener más información sobre los cuadros de diálogo, vea [Cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Paso 1: Crear el cuadro de Owner-Drawn de diálogo

En el ejemplo de código se usa [**la función DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) para crear un cuadro de diálogo modal. La plantilla de cuadro de diálogo IDD SQMEAL define los estilos de ventana, los botones y los identificadores de \_ control del cuadro combinado. El cuadro combinado de este ejemplo usa los estilos [**\_ CBS DROPDOWNLIST**](combo-box-styles.md), [**CBS \_ OWNERDRAWFIXED,**](combo-box-styles.md) [**CBS \_ SORT,**](combo-box-styles.md) [**CBS \_ HASSTRINGS,**](combo-box-styles.md) [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)y [**WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles)


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Paso 2: Procesar los mensajes WM \_ INITDIALOG y WM \_ DESTROY en un cuadro de diálogo.

Cuando se usa un cuadro combinado en un cuadro de diálogo, normalmente se responde a un mensaje [**\_ WM INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) inicializando el cuadro combinado. La aplicación carga los mapas de bits utilizados para el cuadro combinado dibujado por el propietario y, a continuación, llama a la función definida por la aplicación `InitGroupList` para inicializar el cuadro combinado. También selecciona el primer elemento de lista del cuadro combinado y, a continuación, llama a la función definida por la aplicación `InitFoodList` para inicializar el cuadro de lista.

En el ejemplo, el cuadro combinado dibujado por el propietario es un cuadro de lista desplegable que contiene los nombres de cada uno de los cuatro grupos de alimentos. `InitGroupList` agrega el nombre de cada grupo de alimentos y usa el mensaje [**\_ CB SETITEMDATA**](cb-setitemdata.md) para asociar un identificador de mapa de bits a cada elemento de lista que identifica un grupo de alimentos.

El cuadro de lista del ejemplo contiene los nombres de los alimentos del grupo de alimentos seleccionado. **InitFoodList** restablece el contenido del cuadro de lista y, a continuación, agrega los nombres de la selección de alimentos actual en el cuadro de lista desplegable del grupo de alimentos actual.


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



Cuando recibe el mensaje [**WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy) la aplicación elimina los mapas de bits del cuadro combinado dibujado por el propietario.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Paso 3: Procesar el mensaje \_ MEASUREITEM de WM.

Un cuadro combinado dibujado por el propietario envía el mensaje [**\_ MEASUREITEM de WM**](wm-measureitem.md) a su ventana primaria o procedimiento de cuadro de diálogo para que la aplicación pueda establecer las dimensiones de cada elemento de lista. Dado que el cuadro combinado de ejemplo tiene el estilo [**\_ CBS OWNERDRAWFIXED,**](combo-box-styles.md) el sistema envía el **mensaje WM \_ MEASUREITEM** una sola vez. Los cuadros combinados con [**el \_ estilo CBS OWNERDRAWVARIABLE**](combo-box-styles.md) envían un **mensaje WM \_ MEASUREITEM** para cada elemento de lista.

El *parámetro lParam* es un puntero a una [**estructura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica el control y el elemento de lista. También contiene las dimensiones predeterminadas del elemento de lista. En el ejemplo se modifica el miembro de la estructura **itemHeight** para asegurarse de que los elementos de lista son lo suficientemente altos como para alojar los mapas de bits del grupo de alimentos.


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a>Paso 4: Procesar el mensaje \_ DRAWITEM de WM.

Un cuadro combinado dibujado por el propietario envía el mensaje [**\_ DRAWITEM de WM**](wm-drawitem.md) a su ventana primaria o procedimiento de cuadro de diálogo cada vez que la aplicación debe volver a dibujar un elemento de lista. El *parámetro lParam* es un puntero a una [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que identifica el control y el elemento de lista. También contiene la información necesaria para pintar el elemento.

La aplicación de ejemplo muestra el texto del elemento de lista y el mapa de bits asociado al grupo de alimentos. Si el elemento tiene el foco, también dibuja un rectángulo de foco. Antes de mostrar el texto, el ejemplo establece los colores de primer plano y de fondo, en función del elemento seleccionado. Dado que el cuadro combinado tiene el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) el cuadro combinado mantiene el texto de cada elemento de lista que se puede recuperar mediante el mensaje [**\_ GETLBTEXT de CB.**](cb-getlbtext.md)

Los mapas de bits usados para el elemento de lista dependen del grupo de alimentos. `InitGroupList` usa el [**mensaje CB \_ SETITEMDATA para**](cb-setitemdata.md) asociar un identificador de mapa de bits a cada elemento de lista. El procedimiento de ventana recupera el identificador de mapa de bits del **miembro itemData** de la [**estructura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) El sistema usa dos mapas de bits para cada símbolo de grupo de alimentos: un mapa de bits monocromo con la operación de trama SRCAND para borrar la región irregular detrás de la imagen y un mapa de bits de color con la operación de trama SRCPAINT para pintar la imagen.


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a>Paso 5: Procesar el mensaje \_ WM COMMAND.

Cuando se produce un evento en un control de cuadro de diálogo, el control notifica al procedimiento del cuadro de diálogo mediante un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command) En el ejemplo se procesa mensajes de notificación desde el cuadro combinado, el cuadro de lista y el **botón** Aceptar. El identificador de control está en la palabra de orden bajo *de wParam* y el código de notificación está en la palabra de orden superior *de wParam*.

Si el identificador de control es IDCOMBO, se ha producido un evento en el cuadro combinado. En respuesta, el procedimiento del cuadro de diálogo omite todos los demás eventos de cuadro combinado excepto [**CBN \_ SELENDOK,**](cbn-selendok.md)lo que indica que se realizó una selección, que se cerró el cuadro de lista desplegable y que se deben aceptar los cambios realizados. El procedimiento del cuadro de diálogo llama a para restablecer el contenido del cuadro de lista y para agregar los nombres de las selecciones actuales en el `InitFoodList` cuadro de lista desplegable.

Si el identificador de control es IDLIST, se ha producido un evento en el cuadro de lista. Esto hace que el procedimiento del cuadro de diálogo ignore todos los eventos de cuadro de lista excepto [**LBN \_ DBLCLK**](lbn-dblclk.md), lo que indica que el usuario ha hecho doble clic en un elemento de lista. Este evento se procesa de la  misma manera que si se hubiera elegido un botón Aceptar.

Si el identificador de control es IDOK, el usuario ha elegido el **botón** Aceptar. En respuesta, el procedimiento del cuadro de diálogo inserta el nombre de la comida seleccionada en el control de edición de varias líneas de la aplicación y, a continuación, llama a la [**función EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para cerrar el cuadro de diálogo.

Si el identificador de control es IDCANCEL, el usuario ha hecho clic en el **botón** Cancelar. En respuesta, el procedimiento del cuadro de diálogo llama [**a EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para cerrar el cuadro de diálogo.


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a>Ejemplo completo

A continuación se muestra el procedimiento del cuadro de diálogo y las funciones de apoyo para el **cuadro de diálogo Menú** cuadrado.


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar cuadros combinados](using-combo-boxes.md)
</dt> </dl>

 

 