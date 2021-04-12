---
title: Crear un contexto de representación y convertirlo en actual
description: En el ejemplo de código siguiente se muestra cómo crear un contexto de representación de OpenGL en respuesta a un mensaje de creación de WM \_ .
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357394"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Crear un contexto de representación y convertirlo en actual

En el ejemplo de código siguiente se muestra cómo crear un contexto de representación de OpenGL en respuesta a un mensaje de creación de WM \_ . Tenga en cuenta que debe configurar el formato de píxel antes de crear el contexto de representación. Observe también que, en este escenario, el contexto de dispositivo no se libera localmente. se libera cuando se cierra la ventana, después de que el contexto de representación no sea el actual. Para obtener más información, vea [eliminar un contexto de representación](deleting-a-rendering-context.md). Por último, tenga en cuenta que puede usar variables locales para los identificadores de contexto de dispositivo y de representación, ya que con las funciones [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) y [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) puede obtener identificadores para esos contextos según sea necesario.

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




