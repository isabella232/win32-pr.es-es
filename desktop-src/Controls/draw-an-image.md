---
title: Dibujar una imagen
description: En este tema se muestra cómo usar la función ImageList \_ Draw para dibujar una imagen.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b42e97ad9b7cab8693431654dc31b473267414f31ae5811f4f66a6663ce8e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878335"
---
# <a name="how-to-draw-an-image"></a>Dibujar una imagen

En este tema se muestra cómo usar la [**función ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para dibujar una imagen.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para dibujar una imagen, use las funciones [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Especifique el identificador de una lista de imágenes, el índice de la imagen que se va a dibujar, el identificador del contexto del dispositivo de destino, una ubicación dentro del contexto del dispositivo y uno o varios estilos de dibujo.

La función definida por el usuario en el siguiente ejemplo de código de C++ usa la función [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para dibujar una imagen y guarda las coordenadas de cliente del rectángulo delimitador de la imagen. Una función posterior usa el rectángulo delimitador para determinar si el usuario ha hecho clic en la imagen.



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de listas de imágenes](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Acerca de las listas de imágenes](image-lists.md)
</dt> <dt>

[Usar listas de imágenes](using-image-lists.md)
</dt> </dl>

 

 




