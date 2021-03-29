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
# <a name="porting-glx-pixmap-code"></a>Portabilidad de GLX Pixmap Code

El sistema X Window usa *pixmaps*, que son superficies de dibujo virtuales fuera de la pantalla en forma de matriz tridimensional de bits. Puede pensar en un Pixmap como una pila de mapas de bits: una matriz bidimensional de píxeles con cada píxel con un valor comprendido entre 0 y 2N1, donde N es la profundidad de Pixmap.

En el caso de los programas OpenGL, se usan las funciones GLX, **glXCreateGLXPixmap** y **glXDestroyGLXPixmap**, para crear y destruir GLX pixmaps usados para la representación fuera de la pantalla.

Windows usa mapas de bits independientes del dispositivo que sirven para la misma función que X Window System pixmaps. Use las funciones de mapa de bits estándar de Windows para crear y destruir mapas de bits.

En la tabla siguiente se enumeran las funciones de Pixmap de GLX y sus funciones de mapa de bits de Windows equivalentes.



| GLX Pixmap and Font (función)                                                          | Mapa de bits y función de fuente de Windows                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**(display *\* dpy*, XVisualInfo *\* Vis*, Pixmap *Pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint * fuUsage ***)** hBitmap [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**(display *\* dpy*, GLXPixmap *PIX*)                        | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

