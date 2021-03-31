---
title: Trasladar contextos de representación
description: Trasladar contextos de representación
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextos de representación OpenGL, Porting
- OpenGL en Windows, contextos de representación
- trasladar a OpenGL, contextos de representación
- Portabilidad de OpenGL, contextos de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418874"
---
# <a name="porting-rendering-contexts"></a>Trasladar contextos de representación

El sistema de ventanas X y las ventanas se representan a través de contextos de representación. Seis funciones GLX administrar contextos de representación y cinco de ellos tienen una función de Windows equivalente.

En la tabla siguiente se enumeran las funciones de representación de GLX y sus funciones de Windows equivalentes.



| Función de contexto de representación GLX                                                                            | Función de contexto de representación de Windows                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**(display *\* dpy*, GLXContext *src*, GLXContext *DST*, GLuint *Mask*)            | No es aplicable.                                                         |
| GLXContext **glXCreateContext**(display *\* dpy*, XVisualInfo *\* Vis*, GLXContext *shareList*, bool *Direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)          |
| void **glXDeleteContext**(display *\* dpy*, GLXContext *CTX*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)                  |
| Bool **glXMakeCurrent**(display *\* dpy*, GLXDrawable *Draw*, GLXContext *CTX*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*) |



 

Los tipos de valor devuelto y otros tipos tienen nombres diferentes en el sistema de ventana X que en Windows. Puede buscar apariciones de GLXContext para ayudar a encontrar partes del código que deben migrarse.

En las secciones siguientes se comparan los ejemplos de código de contexto de representación en un programa de sistema X Window y el mismo código después de que se haya trasladado a Windows.

Para obtener más información sobre la representación de contextos, vea [contextos de representación](rendering-contexts.md).

 

 




