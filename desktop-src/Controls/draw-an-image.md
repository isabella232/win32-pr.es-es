---
title: Cómo dibujar una imagen
description: En este tema se muestra cómo usar la función de \_ dibujo ImageList para dibujar una imagen.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995764"
---
# <a name="how-to-draw-an-image"></a><span data-ttu-id="a52fc-103">Cómo dibujar una imagen</span><span class="sxs-lookup"><span data-stu-id="a52fc-103">How to Draw an Image</span></span>

<span data-ttu-id="a52fc-104">En este tema se muestra cómo usar la función de [**\_ dibujo ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para dibujar una imagen.</span><span class="sxs-lookup"><span data-stu-id="a52fc-104">This topic demonstrates how to use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a52fc-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="a52fc-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a52fc-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="a52fc-106">Technologies</span></span>

-   [<span data-ttu-id="a52fc-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="a52fc-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a52fc-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a52fc-108">Prerequisites</span></span>

-   <span data-ttu-id="a52fc-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a52fc-109">C/C++</span></span>
-   <span data-ttu-id="a52fc-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="a52fc-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a52fc-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a52fc-111">Instructions</span></span>


<span data-ttu-id="a52fc-112">Para dibujar una imagen, use la función [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) .</span><span class="sxs-lookup"><span data-stu-id="a52fc-112">To draw an image, you use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) or [**ImageList\_DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) function.</span></span> <span data-ttu-id="a52fc-113">Especifique el identificador de una lista de imágenes, el índice de la imagen que se va a dibujar, el identificador del contexto de dispositivo de destino, una ubicación en el contexto del dispositivo y uno o varios estilos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="a52fc-113">You specify the handle to an image list, the index of the image to draw, the handle to the destination device context, a location within the device context, and one or more drawing styles.</span></span>

<span data-ttu-id="a52fc-114">La función definida por el usuario en el siguiente ejemplo de código de C++ utiliza la función de [**\_ dibujo ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para dibujar una imagen y guarda las coordenadas de cliente del rectángulo delimitador de la imagen.</span><span class="sxs-lookup"><span data-stu-id="a52fc-114">The user-defined function in the following C++ code example uses the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image and saves the client coordinates of the image's bounding rectangle.</span></span> <span data-ttu-id="a52fc-115">Una función posterior utiliza el rectángulo delimitador para determinar si el usuario ha hecho clic en la imagen.</span><span class="sxs-lookup"><span data-stu-id="a52fc-115">A subsequent function uses the bounding rectangle to determine whether the user has clicked on the image.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="a52fc-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a52fc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a52fc-117">Referencia de las listas de imágenes</span><span class="sxs-lookup"><span data-stu-id="a52fc-117">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="a52fc-118">Acerca de las listas de imágenes</span><span class="sxs-lookup"><span data-stu-id="a52fc-118">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="a52fc-119">Usar listas de imágenes</span><span class="sxs-lookup"><span data-stu-id="a52fc-119">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 




