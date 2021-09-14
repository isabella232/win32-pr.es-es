---
title: Porte de contextos de representación
description: Porte de contextos de representación
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextos de representación OpenGL , porting
- OpenGL en Windows, contextos de representación
- porte a OpenGL, representación de contextos
- Porte de OpenGL, representación de contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073996"
---
# <a name="porting-rendering-contexts"></a>Porte de contextos de representación

El sistema de ventanas X y Windows a través de contextos de representación. Seis funciones GLX administran contextos de representación y cinco de ellas tienen una función Windows equivalente.

En la tabla siguiente se enumeran las funciones de representación glx y sus funciones de Windows equivalentes.



| Función de contexto de representación GLX                                                                            | Windows de contexto de representación                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**( Display *\* dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)            | No aplicable.                                                         |
| GLXContext **glXCreateContext**( Display *\* dpy*,XVisualInfo *\* vis*,GLXContext *shareList*,Bool *direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)          |
| void **glXDeleteContext**( Display *\* dpy*,GLXContext *ctx*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)                  |
| Bool **glXMakeCurrent**( Display *\* dpy*,GLXDrawable *draw*,GLXContext *ctx*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*, HGLRC *hglrc*) |



 

Los tipos devueltos y otros tipos tienen nombres diferentes en el sistema de ventanas X que en Windows. Puede buscar repeticiones de GLXContext para ayudar a encontrar partes del código que se deben porte.

En las secciones siguientes se comparan ejemplos de código de contexto de representación en un programa del sistema de ventanas X y el mismo código después de que se haya portado a Windows.

Para obtener más información sobre los contextos de representación, vea [Rendering Contexts](rendering-contexts.md).

 

 




