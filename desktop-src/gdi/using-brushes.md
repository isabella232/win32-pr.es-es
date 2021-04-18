---
description: Puede usar un pincel para pintar el interior de prácticamente cualquier forma mediante una función de la interfaz de dispositivo gráfico (GDI).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Uso de pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65ad4b14ba445642f224b0002eb1e7517c1008b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545118"
---
# <a name="using-brushes"></a><span data-ttu-id="f267a-103">Uso de pinceles</span><span class="sxs-lookup"><span data-stu-id="f267a-103">Using Brushes</span></span>

<span data-ttu-id="f267a-104">Puede usar un pincel para pintar el interior de prácticamente cualquier forma mediante una función de la interfaz de dispositivo gráfico (GDI).</span><span class="sxs-lookup"><span data-stu-id="f267a-104">You can use a brush to paint the interior of virtually any shape by using a graphics device interface (GDI) function.</span></span> <span data-ttu-id="f267a-105">Esto incluye los interiores de rectángulos, elipses, polígonos y rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="f267a-105">This includes the interiors of rectangles, ellipses, polygons, and paths.</span></span> <span data-ttu-id="f267a-106">En función de los requisitos de la aplicación, puede usar un pincel sólido de un color especificado, un pincel de bolsa, un pincel de trama o un pincel de trama.</span><span class="sxs-lookup"><span data-stu-id="f267a-106">Depending on the requirements of your application, you can use a solid brush of a specified color, a stock brush, a hatch brush, or a pattern brush.</span></span>

<span data-ttu-id="f267a-107">Esta sección contiene ejemplos de código que muestran la creación de un cuadro de diálogo de pincel personalizado.</span><span class="sxs-lookup"><span data-stu-id="f267a-107">This section contains code samples that demonstrate the creation of a custom brush dialog box.</span></span> <span data-ttu-id="f267a-108">El cuadro de diálogo contiene una cuadrícula que representa el mapa de bits que el sistema utiliza como pincel.</span><span class="sxs-lookup"><span data-stu-id="f267a-108">The dialog box contains a grid that represents the bitmap the system uses as a brush.</span></span> <span data-ttu-id="f267a-109">Un usuario puede utilizar esta cuadrícula para crear un mapa de bits de pincel de patrón y, a continuación, ver el patrón personalizado haciendo clic en el botón **patrón de prueba** .</span><span class="sxs-lookup"><span data-stu-id="f267a-109">A user can use this grid to create a pattern-brush bitmap and then view the custom pattern by clicking the **Test Pattern** button.</span></span>

<span data-ttu-id="f267a-110">En la ilustración siguiente se muestra un patrón creado mediante el cuadro de diálogo **pincel personalizado** .</span><span class="sxs-lookup"><span data-stu-id="f267a-110">The following illustration shows a pattern created by using the **Custom Brush** dialog box.</span></span>

![captura de pantalla del cuadro de diálogo pincel personalizado](images/custbrush.png)

<span data-ttu-id="f267a-112">Para mostrar un cuadro de diálogo, primero debe crear una plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f267a-112">To display a dialog box, you must first create a dialog box template.</span></span> <span data-ttu-id="f267a-113">La siguiente plantilla de cuadro de diálogo define el cuadro de diálogo **pincel personalizado** .</span><span class="sxs-lookup"><span data-stu-id="f267a-113">The following dialog box template defines the **Custom Brush** dialog box.</span></span>


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



<span data-ttu-id="f267a-114">El cuadro de diálogo **pincel personalizado** contiene cinco controles: una ventana de cuadrícula de mapa de bits, una ventana de visualización de patrones y tres botones de control, con la etiqueta **modelo de prueba**, **Aceptar** y **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="f267a-114">The **Custom Brush** dialog box contains five controls: a bitmap-grid window, a pattern-viewing window, and three push buttons, labeled **Test Pattern**, **OK**, and **Cancel**.</span></span> <span data-ttu-id="f267a-115">El botón de preinstalación del **patrón de prueba** permite al usuario ver el patrón.</span><span class="sxs-lookup"><span data-stu-id="f267a-115">The **Test Pattern** push button enables the user to view the pattern.</span></span> <span data-ttu-id="f267a-116">La plantilla de cuadro de diálogo especifica las dimensiones generales de la ventana de cuadro de diálogo, asigna un valor a cada control, especifica la ubicación de cada control, etc.</span><span class="sxs-lookup"><span data-stu-id="f267a-116">The dialog box template specifies the overall dimensions of the dialog box window, assigns a value to each control, specifies the location of each control, and so forth.</span></span> <span data-ttu-id="f267a-117">Para obtener más información, consulte [cuadros de diálogo](../dlgbox/dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="f267a-117">For more information, see [Dialog Boxes](../dlgbox/dialog-boxes.md).</span></span>

<span data-ttu-id="f267a-118">Los valores de control de la plantilla de cuadro de diálogo son constantes que se han definido como se indica a continuación en el archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f267a-118">The control values in the dialog box template are constants that have been defined as follows in the application's header file.</span></span>


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



<span data-ttu-id="f267a-119">Después de crear una plantilla de cuadro de diálogo e incluirla en el archivo de definición de recursos de la aplicación, debe escribir un procedimiento de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f267a-119">After you create a dialog box template and include it in the application's resource-definition file, you must write a dialog procedure.</span></span> <span data-ttu-id="f267a-120">Este procedimiento procesa los mensajes que el sistema envía al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f267a-120">This procedure processes messages that the system sends to the dialog box.</span></span> <span data-ttu-id="f267a-121">En el siguiente fragmento del código fuente de una aplicación se muestra el procedimiento de cuadro de diálogo para el cuadro de diálogo **pincel personalizado** y las dos funciones definidas por la aplicación a las que llama.</span><span class="sxs-lookup"><span data-stu-id="f267a-121">The following excerpt from an application's source code shows the dialog box procedure for the **Custom Brush** dialog box and the two application-defined functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



<span data-ttu-id="f267a-122">El procedimiento de cuadro de diálogo para el cuadro de diálogo **pincel personalizado** procesa cuatro mensajes, tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f267a-122">The dialog box procedure for the **Custom Brush** dialog box processes four messages, as described in the following table.</span></span>



| <span data-ttu-id="f267a-123">Message</span><span class="sxs-lookup"><span data-stu-id="f267a-123">Message</span></span>                                          | <span data-ttu-id="f267a-124">Acción</span><span class="sxs-lookup"><span data-stu-id="f267a-124">Action</span></span>                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f267a-125">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f267a-125">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)   | <span data-ttu-id="f267a-126">Recupera un identificador de ventana y las dimensiones de los controles de la ventana de cuadrícula y del pincel de patrón, calcula las dimensiones de una sola celda en el control de ventana de cuadrícula e inicializa una matriz de coordenadas de celda de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="f267a-126">Retrieves a window handle and dimensions for the grid-window and pattern-brush controls, computes the dimensions of a single cell in the grid-window control, and initializes an array of grid-cell coordinates.</span></span>                                                                                           |
| [<span data-ttu-id="f267a-127">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f267a-127">**WM\_PAINT**</span></span>](wm-paint.md)                    | <span data-ttu-id="f267a-128">Dibuja el patrón de cuadrícula en el control de ventana de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="f267a-128">Draws the grid pattern in the grid-window control.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f267a-129">**LBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f267a-129">**WM\_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md) | <span data-ttu-id="f267a-130">Determina si el cursor se encuentra dentro del control de ventana de cuadrícula cuando el usuario presiona el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="f267a-130">Determines whether the cursor is within the grid-window control when the user presses the left mouse button.</span></span> <span data-ttu-id="f267a-131">Si es así, el procedimiento de cuadro de diálogo invierte la celda de cuadrícula adecuada y registra el estado de esa celda en una matriz de bits que se usa para crear el mapa de bits para el pincel personalizado.</span><span class="sxs-lookup"><span data-stu-id="f267a-131">If so, the dialog box procedure inverts the appropriate grid cell and records the state of that cell in an array of bits that is used to create the bitmap for the custom brush.</span></span>              |
| [<span data-ttu-id="f267a-132">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f267a-132">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)         | <span data-ttu-id="f267a-133">Procesa la entrada para los tres controles de botón de control.</span><span class="sxs-lookup"><span data-stu-id="f267a-133">Processes input for the three push button controls.</span></span> <span data-ttu-id="f267a-134">Si el usuario hace clic en el botón **patrón de prueba** , el procedimiento del cuadro de diálogo pinta el control patrón de prueba con el nuevo patrón de pincel personalizado.</span><span class="sxs-lookup"><span data-stu-id="f267a-134">If the user clicks the **Test Pattern** button, the dialog box procedure paints the Test Pattern control with the new custom brush pattern.</span></span> <span data-ttu-id="f267a-135">Si el usuario hace clic en el botón **Aceptar** o **Cancelar** , el procedimiento del cuadro de diálogo realiza acciones según corresponda.</span><span class="sxs-lookup"><span data-stu-id="f267a-135">If the user clicks the **OK** or **Cancel** button, the dialog box procedure performs actions accordingly.</span></span> |



 

<span data-ttu-id="f267a-136">Para obtener más información acerca de los mensajes y el procesamiento de mensajes, consulte [mensajes y colas](../winmsg/messages-and-message-queues.md)de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f267a-136">For more information about messages and message processing, see [Messages and Message Queues](../winmsg/messages-and-message-queues.md).</span></span>

<span data-ttu-id="f267a-137">Después de escribir el procedimiento del cuadro de diálogo, incluya la definición de función para el procedimiento en el archivo de encabezado de la aplicación y, a continuación, llame al procedimiento del cuadro de diálogo en el punto adecuado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f267a-137">After you write the dialog box procedure, include the function definition for the procedure in the application's header file and then call the dialog box procedure at the appropriate point in the application.</span></span>

<span data-ttu-id="f267a-138">En el siguiente fragmento del archivo de encabezado de la aplicación se muestra la definición de función para el procedimiento de cuadro de diálogo y las dos funciones a las que llama.</span><span class="sxs-lookup"><span data-stu-id="f267a-138">The following excerpt from the application's header file shows the function definition for the dialog box procedure and the two functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



<span data-ttu-id="f267a-139">Por último, el código siguiente muestra cómo se llama al procedimiento de cuadro de diálogo desde el archivo de código fuente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f267a-139">Finally, the following code shows how the dialog box procedure is called from the application's source-code file.</span></span>


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



<span data-ttu-id="f267a-140">Normalmente, esta llamada se realiza en respuesta al usuario que elige una opción en el menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f267a-140">This call is usually made in response to the user choosing an option from the application's menu.</span></span>

 

 
