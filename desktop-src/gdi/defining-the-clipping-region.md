---
description: Cuando el usuario hace clic en definir la región de recorte, el sistema emite un mensaje de comando de WM \_ .
ms.assetid: 4b20f310-98c0-42c1-b3b3-eadf9bb2003c
title: Definir la región de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e49693c0e94ab9b43af817f80985af98ae2ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544531"
---
# <a name="defining-the-clipping-region"></a><span data-ttu-id="255be-103">Definir la región de recorte</span><span class="sxs-lookup"><span data-stu-id="255be-103">Defining the Clipping Region</span></span>

<span data-ttu-id="255be-104">Cuando el usuario hace clic en definir la región de recorte, el sistema emite un mensaje de [**\_ comando de WM**](../menurc/wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="255be-104">When the user clicks Define Clip Region , the system issues a [**WM\_COMMAND**](../menurc/wm-command.md) message.</span></span> <span data-ttu-id="255be-105">El parámetro *wParam* de este mensaje contiene una constante definida por la aplicación, de la definición de IDM \_ , que indica que el usuario seleccionó esta opción en el menú.</span><span class="sxs-lookup"><span data-stu-id="255be-105">The *wParam* parameter of this message contains an application-defined constant, IDM\_DEFINE, that indicates that the user selected this option from the menu.</span></span> <span data-ttu-id="255be-106">La aplicación procesa esta entrada estableciendo una marca booleana, fDefineRegion, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="255be-106">The application processes this input by setting a Boolean flag, fDefineRegion, as shown in the following code sample.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
 
        case IDM_DEFINE: 
            fDefineRegion = TRUE; 
            break; 
```



<span data-ttu-id="255be-107">Después de hacer clic en **definir la región de recorte** , el usuario puede empezar a dibujar el rectángulo haciendo clic y arrastrando el mouse mientras el cursor se encuentra en el área cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="255be-107">After clicking **Define Clipping Region** , the user can begin drawing the rectangle by clicking and dragging the mouse while the cursor is in the application's client area.</span></span>

<span data-ttu-id="255be-108">Cuando el usuario presiona el botón primario, el sistema emite un mensaje de [**\_ LBUTTONDOWN de WM**](../inputdev/wm-lbuttondown.md) .</span><span class="sxs-lookup"><span data-stu-id="255be-108">When the user presses the left button, the system issues a [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message.</span></span> <span data-ttu-id="255be-109">El parámetro *lParam* de este mensaje contiene las coordenadas del cursor, que corresponden a la esquina superior izquierda de un rectángulo que se usa para definir la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="255be-109">The *lParam* parameter of this message contains the cursor coordinates, which correspond to the upper left corner of a rectangle used to define the clipping region.</span></span> <span data-ttu-id="255be-110">La aplicación procesa el mensaje de **\_ LBUTTONDOWN de WM** , como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="255be-110">The application processes the **WM\_LBUTTONDOWN** message, as follows.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
switch (message) 
{ 
 
    case WM_LBUTTONDOWN: 
        if (fDefineRegion) 
        { 
 
        // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
 
        if (fRegionExists) 
        { 
 
            // Erase the previous rectangle.  
 
            hdc = GetDC(hwnd); 
            SetROP2(hdc, R2_NOTXORPEN); 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
            ReleaseDC(hwnd, hdc); 
 
            // Clear the rectangle coordinates.  
 
            for (i = 0; i < 4; i++) 
            { 
                aptRect[i].x = 0; 
                aptRect[i].y = 0; 
            } 
 
            // Clear the temporary point structure.  
 
            ptTmp.x = 0; 
            ptTmp.y = 0; 
 
            // Clear the lower right coordinates.  
 
            ptLowerRight.x = 0; 
            ptLowerRight.y = 0; 
 
            // Reset the flag.  
 
            fRegionExists = FALSE; 
            fDefineRegion = TRUE; 
 
            // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
    break; 
}
```



<span data-ttu-id="255be-111">Cuando el usuario arrastra el mouse, el sistema emite mensajes de [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) y almacena las nuevas coordenadas del cursor en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="255be-111">As the user drags the mouse, the system issues [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages and stores the new cursor coordinates in the *lParam* parameter.</span></span> <span data-ttu-id="255be-112">Cada vez que la aplicación recibe un nuevo mensaje de de **WM \_ MOUSEMOVE** , borra el rectángulo anterior (si existe) y dibuja el nuevo rectángulo mediante una llamada a la función [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , pasándole las coordenadas de las cuatro esquinas del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="255be-112">Each time the application receives a new **WM\_MOUSEMOVE** message, it erases the previous rectangle (if one exists) and draws the new rectangle by calling the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function, passing it the coordinates of the four corners of the rectangle.</span></span> <span data-ttu-id="255be-113">La aplicación realiza las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="255be-113">The application performs the following tasks.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
switch (message) 
{ 
 
    case WM_MOUSEMOVE: 
 
    if (wParam & MK_LBUTTON && fDefineRegion) 
    { 
 
        // Get a window DC.  
 
        hdc = GetDC(hwnd); 
 
        if (!SetROP2(hdc, R2_NOTXORPEN)) 
            errhandler("SetROP2 Failed", hwnd); 
 
        // If previous mouse movement occurred, store the original  
        // lower right corner coordinates in a temporary structure.  
 
        if (ptLowerRight.x) 
        { 
            ptTmp.x = ptLowerRight.x; 
            ptTmp.y = ptLowerRight.y; 
        } 
 
        // Get the new coordinates of the clipping region's lower  
        // right corner.  
 
        ptsTmp = MAKEPOINTS(lParam); 
        ptLowerRight.x = (LONG) ptsTmp.x; 
        ptLowerRight.y = (LONG) ptsTmp.y; 
 
        // If previous mouse movement occurred, erase the original  
        // rectangle.  
 
        if (ptTmp.x) 
        { 
            aptRect[0].x = ptUpperLeft.x; 
            aptRect[0].y = ptUpperLeft.y; 
            aptRect[1].x = ptTmp.x; 
            aptRect[1].y = ptUpperLeft.y; 
            aptRect[2].x = ptTmp.x; 
            aptRect[2].y = ptTmp.y; 
            aptRect[3].x = ptUpperLeft.x; 
            aptRect[3].y = ptTmp.y; 
            aptRect[4].x = aptRect[0].x; 
            aptRect[4].y = aptRect[0].y; 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
        } 
 
        aptRect[0].x = ptUpperLeft.x; 
        aptRect[0].y = ptUpperLeft.y; 
        aptRect[1].x = ptLowerRight.x; 
        aptRect[1].y = ptUpperLeft.y; 
        aptRect[2].x = ptLowerRight.x; 
        aptRect[2].y = ptLowerRight.y; 
        aptRect[3].x = ptUpperLeft.x; 
        aptRect[3].y = ptLowerRight.y; 
        aptRect[4].x = aptRect[0].x; 
        aptRect[4].y = aptRect[0].y; 
 
        if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
             errhandler("Polyline Failed", hwnd); 
 
        ReleaseDC(hwnd, hdc); 
    } 
    break; 
```



 

 
