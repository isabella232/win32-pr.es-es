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
# <a name="using-brushes"></a>Uso de pinceles

Puede usar un pincel para pintar el interior de prácticamente cualquier forma mediante una función de la interfaz de dispositivo gráfico (GDI). Esto incluye los interiores de rectángulos, elipses, polígonos y rutas de acceso. En función de los requisitos de la aplicación, puede usar un pincel sólido de un color especificado, un pincel de bolsa, un pincel de trama o un pincel de trama.

Esta sección contiene ejemplos de código que muestran la creación de un cuadro de diálogo de pincel personalizado. El cuadro de diálogo contiene una cuadrícula que representa el mapa de bits que el sistema utiliza como pincel. Un usuario puede utilizar esta cuadrícula para crear un mapa de bits de pincel de patrón y, a continuación, ver el patrón personalizado haciendo clic en el botón **patrón de prueba** .

En la ilustración siguiente se muestra un patrón creado mediante el cuadro de diálogo **pincel personalizado** .

![captura de pantalla del cuadro de diálogo pincel personalizado](images/custbrush.png)

Para mostrar un cuadro de diálogo, primero debe crear una plantilla de cuadro de diálogo. La siguiente plantilla de cuadro de diálogo define el cuadro de diálogo **pincel personalizado** .


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



El cuadro de diálogo **pincel personalizado** contiene cinco controles: una ventana de cuadrícula de mapa de bits, una ventana de visualización de patrones y tres botones de control, con la etiqueta **modelo de prueba**, **Aceptar** y **Cancelar**. El botón de preinstalación del **patrón de prueba** permite al usuario ver el patrón. La plantilla de cuadro de diálogo especifica las dimensiones generales de la ventana de cuadro de diálogo, asigna un valor a cada control, especifica la ubicación de cada control, etc. Para obtener más información, consulte [cuadros de diálogo](../dlgbox/dialog-boxes.md).

Los valores de control de la plantilla de cuadro de diálogo son constantes que se han definido como se indica a continuación en el archivo de encabezado de la aplicación.


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



Después de crear una plantilla de cuadro de diálogo e incluirla en el archivo de definición de recursos de la aplicación, debe escribir un procedimiento de diálogo. Este procedimiento procesa los mensajes que el sistema envía al cuadro de diálogo. En el siguiente fragmento del código fuente de una aplicación se muestra el procedimiento de cuadro de diálogo para el cuadro de diálogo **pincel personalizado** y las dos funciones definidas por la aplicación a las que llama.


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



El procedimiento de cuadro de diálogo para el cuadro de diálogo **pincel personalizado** procesa cuatro mensajes, tal y como se describe en la tabla siguiente.



| Message                                          | Acción                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INITDIALOG de WM \_**](../dlgbox/wm-initdialog.md)   | Recupera un identificador de ventana y las dimensiones de los controles de la ventana de cuadrícula y del pincel de patrón, calcula las dimensiones de una sola celda en el control de ventana de cuadrícula e inicializa una matriz de coordenadas de celda de cuadrícula.                                                                                           |
| [**pintura de WM \_**](wm-paint.md)                    | Dibuja el patrón de cuadrícula en el control de ventana de cuadrícula.                                                                                                                                                                                                                                                         |
| [**LBUTTONDOWN de WM \_**](../inputdev/wm-lbuttondown.md) | Determina si el cursor se encuentra dentro del control de ventana de cuadrícula cuando el usuario presiona el botón primario del mouse. Si es así, el procedimiento de cuadro de diálogo invierte la celda de cuadrícula adecuada y registra el estado de esa celda en una matriz de bits que se usa para crear el mapa de bits para el pincel personalizado.              |
| [**comando de WM \_**](../menurc/wm-command.md)         | Procesa la entrada para los tres controles de botón de control. Si el usuario hace clic en el botón **patrón de prueba** , el procedimiento del cuadro de diálogo pinta el control patrón de prueba con el nuevo patrón de pincel personalizado. Si el usuario hace clic en el botón **Aceptar** o **Cancelar** , el procedimiento del cuadro de diálogo realiza acciones según corresponda. |



 

Para obtener más información acerca de los mensajes y el procesamiento de mensajes, consulte [mensajes y colas](../winmsg/messages-and-message-queues.md)de mensajes.

Después de escribir el procedimiento del cuadro de diálogo, incluya la definición de función para el procedimiento en el archivo de encabezado de la aplicación y, a continuación, llame al procedimiento del cuadro de diálogo en el punto adecuado de la aplicación.

En el siguiente fragmento del archivo de encabezado de la aplicación se muestra la definición de función para el procedimiento de cuadro de diálogo y las dos funciones a las que llama.


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



Por último, el código siguiente muestra cómo se llama al procedimiento de cuadro de diálogo desde el archivo de código fuente de la aplicación.


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



Normalmente, esta llamada se realiza en respuesta al usuario que elige una opción en el menú de la aplicación.

 

 
