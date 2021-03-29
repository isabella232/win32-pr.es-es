---
title: Portabilidad de GLX Pixmap Code
description: Portabilidad de GLX Pixmap Code
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- OpenGL en Windows, pixmaps
- trasladar a OpenGL, pixmaps
- Portabilidad de OpenGL, pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078291"
---
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="20ce1-107">Portabilidad de GLX Pixmap Code</span><span class="sxs-lookup"><span data-stu-id="20ce1-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="20ce1-108">El sistema X Window usa *pixmaps*, que son superficies de dibujo virtuales fuera de la pantalla en forma de matriz tridimensional de bits.</span><span class="sxs-lookup"><span data-stu-id="20ce1-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="20ce1-109">Puede pensar en un Pixmap como una pila de mapas de bits: una matriz bidimensional de píxeles con cada píxel con un valor comprendido entre 0 y 2N1, donde N es la profundidad de Pixmap.</span><span class="sxs-lookup"><span data-stu-id="20ce1-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="20ce1-110">En el caso de los programas OpenGL, se usan las funciones GLX, **glXCreateGLXPixmap** y **glXDestroyGLXPixmap**, para crear y destruir GLX pixmaps usados para la representación fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="20ce1-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="20ce1-111">Windows usa mapas de bits independientes del dispositivo que sirven para la misma función que X Window System pixmaps.</span><span class="sxs-lookup"><span data-stu-id="20ce1-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="20ce1-112">Use las funciones de mapa de bits estándar de Windows para crear y destruir mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="20ce1-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="20ce1-113">En la tabla siguiente se enumeran las funciones de Pixmap de GLX y sus funciones de mapa de bits de Windows equivalentes.</span><span class="sxs-lookup"><span data-stu-id="20ce1-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="20ce1-114">GLX Pixmap and Font (función)</span><span class="sxs-lookup"><span data-stu-id="20ce1-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="20ce1-115">Mapa de bits y función de fuente de Windows</span><span class="sxs-lookup"><span data-stu-id="20ce1-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ce1-116">GLXPixmap **glXCreateGLXPixmap**(display *\* dpy*, XVisualInfo *\* Vis*, Pixmap *Pixmap*)</span><span class="sxs-lookup"><span data-stu-id="20ce1-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="20ce1-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint \* fuUsage \***)** hBitmap [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)</span><span class="sxs-lookup"><span data-stu-id="20ce1-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="20ce1-118">void **glXDestroyGLXPixmap**(display *\* dpy*, GLXPixmap *PIX*)</span><span class="sxs-lookup"><span data-stu-id="20ce1-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="20ce1-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)</span><span class="sxs-lookup"><span data-stu-id="20ce1-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

