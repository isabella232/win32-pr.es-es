---
title: Cómo arrastrar una imagen
description: En este tema se muestra cómo arrastrar una imagen en la pantalla. Las funciones de arrastre mueven una imagen sin problemas, en color y sin parpadear el cursor. Se pueden arrastrar imágenes enmascaradas y sin máscara.
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdcbc5af1ad148dafc77a775e7ee901ce8c4d07221ab1e55fca251e51241fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062945"
---
# <a name="how-to-drag-an-image"></a>Cómo arrastrar una imagen

En este tema se muestra cómo arrastrar una imagen en la pantalla. Las funciones de arrastre mueven una imagen sin problemas, en color y sin parpadear el cursor. Se pueden arrastrar imágenes enmascaradas y sin máscara.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="step-1-begin-the-drag-operation"></a>Paso 1: Iniciar la operación de arrastre.

Use la [**función ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) para iniciar una operación de arrastre.

La función definida por el usuario en el siguiente ejemplo de código de C++ está pensada para llamarse en respuesta a un mensaje de botón del mouse, como [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). La función determina si el usuario ha hecho clic en el rectángulo delimitador de la imagen. Si el usuario ha hecho clic, la función captura la entrada del mouse, borra la imagen del área de cliente y calcula la posición de la zona de acceso más reciente dentro de la imagen. La función establece la zona de acceso directo para que coincida con la zona de acceso directo del cursor del mouse. A continuación, la función comienza la operación de arrastre llamando [**a ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a>Paso 2: Mover la imagen.

La [**función ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) mueve la imagen a una nueva ubicación.

La función definida por el usuario en el siguiente ejemplo de código de C++ está pensada para llamarse en respuesta al [**mensaje \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) de WM. Arrastra la imagen a una nueva ubicación.


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a>Paso 3: Finalizar la operación de arrastre.

La función definida por el usuario en el siguiente ejemplo de código de C++ llama a la [**función ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) para finalizar la operación de arrastre. A continuación, llama a [**la función \_ ImageList DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) para desbloquear la ventana y ocultar la imagen de arrastre, lo que permite actualizar la ventana.


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de listas de imágenes](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Acerca de las listas de imágenes](image-lists.md)
</dt> <dt>

[Uso de listas de imágenes](using-image-lists.md)
</dt> </dl>

 

 