---
title: Cómo crear un Owner-Drawn cuadro combinado
description: En este tema se muestra cómo usar un cuadro combinado dibujado por el propietario.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078403"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="342d0-103">Cómo crear un Owner-Drawn cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="342d0-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="342d0-104">En este tema se muestra cómo usar un cuadro combinado dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="342d0-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="342d0-105">En el ejemplo de código de C++ se usa un cuadro de lista desplegable dibujado por el propietario para mostrar los cuatro grupos de alimentos, cada uno representado por un mapa de bits y un nombre.</span><span class="sxs-lookup"><span data-stu-id="342d0-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="342d0-106">Al seleccionar un grupo de alimentos, los alimentos de ese grupo aparecen en una lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![captura de pantalla que muestra un cuadro de diálogo con un cuadro de lista y un cuadro de lista desplegable expandido que muestra un icono y una etiqueta para cada elemento](images/cscbx-01.png)

<span data-ttu-id="342d0-108">El cuadro de diálogo también contiene un cuadro de lista (IDLIST) y dos botones: **Aceptar** (IDOK) y **Cancelar** (IDCANCEL).</span><span class="sxs-lookup"><span data-stu-id="342d0-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="342d0-109">Los archivos de encabezado del SDK definen las constantes IDOK y IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="342d0-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="342d0-110">La constante IDLIST se define en el archivo de encabezado de la aplicación, como es el identificador de control, IDCOMBO.</span><span class="sxs-lookup"><span data-stu-id="342d0-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="342d0-111">Para obtener más información acerca de los cuadros de diálogo, vea [cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes).</span><span class="sxs-lookup"><span data-stu-id="342d0-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="342d0-112">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="342d0-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="342d0-113">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="342d0-113">Technologies</span></span>

-   [<span data-ttu-id="342d0-114">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="342d0-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="342d0-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="342d0-115">Prerequisites</span></span>

-   <span data-ttu-id="342d0-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="342d0-116">C/C++</span></span>
-   <span data-ttu-id="342d0-117">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="342d0-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="342d0-118">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="342d0-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="342d0-119">Paso 1: crear el cuadro de diálogo Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="342d0-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="342d0-120">En el ejemplo de código se usa la función [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) para crear un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="342d0-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="342d0-121">La plantilla de cuadro de diálogo, IDD \_ SQMEAL, define los estilos de ventana, los botones y los identificadores de control para el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="342d0-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="342d0-122">El cuadro combinado de este ejemplo usa los [**estilos \_ CBS DROPDOWNLIST**](combo-box-styles.md), [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md), [**CBS \_ Sort**](combo-box-styles.md), [**CBS \_ HASSTRINGS**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)y [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="342d0-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="342d0-123">Paso 2: procesar los \_ mensajes de WM INITDIALOG y WM \_ Destroy en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="342d0-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="342d0-124">Cuando se usa un cuadro combinado en un cuadro de diálogo, normalmente se responde a un mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) inicializando el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="342d0-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="342d0-125">La aplicación carga los mapas de bits utilizados para el cuadro combinado dibujado por el propietario y, a continuación, llama a la función definida por la aplicación `InitGroupList` para inicializar el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="342d0-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="342d0-126">También selecciona el primer elemento de la lista en el cuadro combinado y, a continuación, llama a la función definida por la aplicación `InitFoodList` para inicializar el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="342d0-127">En el ejemplo, el cuadro combinado dibujado por el propietario es un cuadro de lista desplegable que contiene los nombres de cada uno de los cuatro grupos de alimentos.</span><span class="sxs-lookup"><span data-stu-id="342d0-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="342d0-128">`InitGroupList` agrega el nombre de cada grupo de alimentos y usa el mensaje [**CB \_ SETITEMDATA**](cb-setitemdata.md) para asociar un identificador de mapa de bits a cada elemento de la lista que identifica un grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="342d0-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="342d0-129">El cuadro de lista del ejemplo contiene los nombres de los alimentos del grupo de alimentos seleccionado.</span><span class="sxs-lookup"><span data-stu-id="342d0-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="342d0-130">**InitFoodList** restablece el contenido del cuadro de lista y, a continuación, agrega los nombres de la selección de alimentos actual en el cuadro de lista desplegable grupo de alimentos actual.</span><span class="sxs-lookup"><span data-stu-id="342d0-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


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



<span data-ttu-id="342d0-131">Cuando recibe el mensaje [**de \_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) , la aplicación elimina los mapas de bits en el cuadro combinado dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="342d0-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="342d0-132">Paso 3: procesar el mensaje de MEASUREITEM de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="342d0-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="342d0-133">Un cuadro combinado dibujado por el propietario envía el mensaje de [**\_ MEASUREITEM de WM**](wm-measureitem.md) a su ventana primaria o procedimiento de cuadro de diálogo para que la aplicación pueda establecer las dimensiones de cada elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="342d0-134">Dado que el cuadro combinado de ejemplo tiene el estilo de la [**INE de CBS \_**](combo-box-styles.md) , el sistema envía el mensaje de **WM \_ MEASUREITEM** una sola vez.</span><span class="sxs-lookup"><span data-stu-id="342d0-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="342d0-135">Los cuadros combinados con el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) envían un mensaje de **WM \_ MEASUREITEM** para cada elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="342d0-136">El parámetro *lParam* es un puntero a una estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica el control y el elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="342d0-137">También contiene las dimensiones predeterminadas del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="342d0-138">En el ejemplo se modifica el miembro de la estructura **ItemHeight** para asegurarse de que los elementos de lista son lo suficientemente altos como para dar cabida a los mapas de bits del grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="342d0-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


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



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="342d0-139">Paso 4: procesar el mensaje de la DRAWITEM de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="342d0-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="342d0-140">Un cuadro combinado dibujado por el propietario envía el mensaje de la aplicación de [**WM \_**](wm-drawitem.md) a su ventana primaria o al procedimiento del cuadro de diálogo cada vez que la aplicación debe volver a dibujar un elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="342d0-141">El parámetro *lParam* es un puntero a una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que identifica el control y el elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="342d0-142">También contiene información necesaria para pintar el elemento.</span><span class="sxs-lookup"><span data-stu-id="342d0-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="342d0-143">En la aplicación de ejemplo se muestra el texto del elemento de lista y el mapa de bits asociado al grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="342d0-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="342d0-144">Si el elemento tiene el foco, también dibuja un rectángulo de foco.</span><span class="sxs-lookup"><span data-stu-id="342d0-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="342d0-145">Antes de mostrar el texto, el ejemplo establece los colores de primer plano y de fondo, en función del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="342d0-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="342d0-146">Dado que el cuadro combinado tiene el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el cuadro combinado mantiene el texto de cada elemento de lista que se puede recuperar mediante el mensaje [**CB \_ GETLBTEXT**](cb-getlbtext.md) .</span><span class="sxs-lookup"><span data-stu-id="342d0-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="342d0-147">Los mapas de bits utilizados para el elemento de lista dependen del grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="342d0-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="342d0-148">`InitGroupList` usa el mensaje [**CB \_ SETITEMDATA**](cb-setitemdata.md) para asociar un identificador de mapa de bits a cada elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="342d0-149">El procedimiento de ventana recupera el identificador de mapa de bits del miembro **itemData** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="342d0-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="342d0-150">El sistema utiliza dos mapas de bits para cada símbolo de grupo de alimentos: un mapa de bits monocromo con la operación de SRCAND Raster para borrar la región irregular detrás de la imagen y un mapa de bits de color con la operación de SRCPAINT Raster para pintar la imagen.</span><span class="sxs-lookup"><span data-stu-id="342d0-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


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



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="342d0-151">Paso 5: procesar el mensaje del comando de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="342d0-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="342d0-152">Cuando se produce un evento en un control de cuadro de diálogo, el control notifica el procedimiento de cuadro de diálogo por medio de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="342d0-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="342d0-153">En el ejemplo se procesan los mensajes de notificación desde el cuadro combinado, el cuadro de lista y el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="342d0-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="342d0-154">El identificador de control está en la palabra de orden inferior de *wParam* y el código de notificación está en la palabra de orden superior de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="342d0-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="342d0-155">Si el identificador del control es IDCOMBO, se ha producido un evento en el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="342d0-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="342d0-156">En respuesta, el procedimiento de cuadro de diálogo omite todos los demás eventos de cuadro combinado excepto [**CBN \_ SELENDOK**](cbn-selendok.md), que indica que se ha realizado una selección, el cuadro de lista desplegable se ha cerrado y se deben aceptar los cambios realizados.</span><span class="sxs-lookup"><span data-stu-id="342d0-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="342d0-157">El procedimiento de cuadro de diálogo llama `InitFoodList` a para restablecer el contenido del cuadro de lista y para agregar los nombres de las selecciones actuales en el cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="342d0-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="342d0-158">Si el identificador del control es IDLIST, se ha producido un evento en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="342d0-159">Esto hace que el procedimiento de cuadro de diálogo omita todos los eventos de cuadro de lista excepto [**LBN \_ DBLCLK**](lbn-dblclk.md), lo que indica que el usuario ha haga doble clic en un elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="342d0-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="342d0-160">Este evento se procesa de la misma manera que si se hubiese elegido un botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="342d0-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="342d0-161">Si el identificador del control es IDOK, el usuario ha elegido el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="342d0-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="342d0-162">En respuesta, el procedimiento de cuadro de diálogo inserta el nombre del alimento seleccionado en el control de edición multilínea de la aplicación y, a continuación, llama a la función [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="342d0-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="342d0-163">Si el identificador del control es IDCANCEL, el usuario hizo clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="342d0-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="342d0-164">En respuesta, el procedimiento de cuadro de diálogo llama a [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="342d0-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


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



## <a name="complete-example"></a><span data-ttu-id="342d0-165">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="342d0-165">Complete example</span></span>

<span data-ttu-id="342d0-166">A continuación, se indican el procedimiento de cuadro de diálogo y las funciones auxiliares para el cuadro de diálogo **comida cuadrada** .</span><span class="sxs-lookup"><span data-stu-id="342d0-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


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


## <a name="related-topics"></a><span data-ttu-id="342d0-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="342d0-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="342d0-168">Usar cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="342d0-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 