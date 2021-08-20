---
title: Porting GLXMap Code
description: Porting GLXMap Code
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- maps demaps
- OpenGL en Windows,maps
- porting to OpenGL,maps
- Porte de OpenGL,maps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e50448c254b8d3e01097f1faec2b4df8aeed56be8ae3abb4f5ce13432582559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012063"
---
# <a name="porting-glx-pixmap-code"></a>Porting GLXMap Code

El sistema de ventanas X usa mapas de colores , que son *superficies* de dibujo virtuales fuera de la pantalla en forma de una matriz tridimensional de bits. Puede pensar en un mapa de colores como una pila de mapas de bits: una matriz bidimensional de píxeles con cada píxel con un valor de 0 a 2N1, donde N es la profundidad del mapa de colores.

En el caso de los programas OpenGL, se usan las funciones GLX, **glXCreateGLXPixmap** y **glXDestroyGLXPixmap**, para crear y destruir mapas de objetos glX usados para la representación fuera de la pantalla.

Windows mapas de bits independientes del dispositivo que cumplen la misma función que los mapas del sistema de ventanas X. Use el estándar Windows de mapa de bits para crear y destruir mapas de bits.

En la tabla siguiente se enumeran las funciones glxmap y sus funciones de mapa Windows mapa de bits equivalentes.



| Función glxmap y font                                                          | Windows mapa de bits y función de fuente                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**( Display *\* dpy*,XVisualInfo *\* vis*,Mapmapmap *)* | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) *HDC hdc*, LPBITMAPINFOHEADER *lpbmbm ,DWORD* *fdwInit*,CONST BYTE *\* lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**( Display *\* dpy*,GLXPixmap *pixel*)                        | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

