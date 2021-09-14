---
title: Traducción de la biblioteca GLX
description: Traducción de la biblioteca GLX
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL en Windows,biblioteca GLX
- porting to OpenGL,GLX library
- Porte de OpenGL, biblioteca GLX
- Biblioteca GLX OpenGL
- Funciones de Xlib OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cede2b74dc2881f867370744ee14c00cceba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361991"
---
# <a name="translating-the-glx-library"></a>Traducción de la biblioteca GLX

Los programas del sistema de ventanas X de OpenGL usan la extensión OpenGL con la biblioteca X Window System (GLX). La biblioteca es un conjunto de funciones y rutinas que inicializan el formato de píxel, controlan la representación y realizan otras tareas específicas de OpenGL. Conecta la biblioteca OpenGL al sistema de ventanas X mediante la administración de identificadores de ventana y la representación de contextos. Debe traducir estas funciones a sus funciones de Windows equivalentes. En la tabla siguiente se enumeran las funciones GLX del sistema de ventanas X y sus funciones Windows equivalentes.



| Función GLX/Xlib         | Windows función                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyContext**        | No aplicable.                                                                                                                                        |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glXIsDirect**           | No aplicable.                                                                                                                                        |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glXQueryExtension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**GetDC,**](/windows/desktop/api/winuser/nf-winuser-getdc) [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| No aplicable.           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Algunas funciones GLX no tienen una función Windows equivalente. Para portabilidad de estas funciones Windows, vuelva a escribir el código para lograr la misma funcionalidad. Por ejemplo, **glXWaitGL** no tiene ninguna función Windows equivalente, pero puede lograr el mismo resultado, ejecutando los comandos openGL pendientes mediante una llamada a [**glFinish**](glfinish.md).

En los temas siguientes se describe cómo portabilidad de funciones GLX que establecen el formato de píxel y administran contextos de representación, mapas de mapas y mapas de bits.

 

 