---
title: Crear un contexto de representación y hacer que sea actual
description: En el ejemplo de código siguiente se muestra cómo crear un contexto de representación de OpenGL en respuesta a un mensaje \_ WM CREATE.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260303"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Crear un contexto de representación y hacer que sea actual

En el ejemplo de código siguiente se muestra cómo crear un contexto de representación de OpenGL en respuesta a un mensaje \_ WM CREATE. Tenga en cuenta que configura el formato de píxel antes de crear el contexto de representación. Observe también que, en este escenario, el contexto del dispositivo no se libera localmente; se libera cuando se cierra la ventana, después de hacer que el contexto de representación no sea actual. Para obtener más información, vea [Eliminar un contexto de representación.](deleting-a-rendering-context.md) Por último, tenga en cuenta que puede usar variables locales para el contexto del dispositivo y los identificadores de contexto de representación, ya que con las funciones [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) y [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) puede obtener identificadores para esos contextos según sea necesario.

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

 

 




