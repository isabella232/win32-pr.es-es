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
# <a name="creating-a-rendering-context-and-making-it-current"></a><span data-ttu-id="37231-105">Crear un contexto de representación y convertirlo en actual</span><span class="sxs-lookup"><span data-stu-id="37231-105">Creating a Rendering Context and Making It Current</span></span>

<span data-ttu-id="37231-106">En el ejemplo de código siguiente se muestra cómo crear un contexto de representación de OpenGL en respuesta a un mensaje de creación de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="37231-106">The following code sample shows how to create an OpenGL rendering context in response to a WM\_CREATE message.</span></span> <span data-ttu-id="37231-107">Tenga en cuenta que debe configurar el formato de píxel antes de crear el contexto de representación.</span><span class="sxs-lookup"><span data-stu-id="37231-107">Notice that you set up the pixel format before creating the rendering context.</span></span> <span data-ttu-id="37231-108">Observe también que, en este escenario, el contexto de dispositivo no se libera localmente. se libera cuando se cierra la ventana, después de que el contexto de representación no sea el actual.</span><span class="sxs-lookup"><span data-stu-id="37231-108">Also notice that in this scenario the device context is not released locally; you release it when the window is closed, after making the rendering context not current.</span></span> <span data-ttu-id="37231-109">Para obtener más información, vea [eliminar un contexto de representación](deleting-a-rendering-context.md).</span><span class="sxs-lookup"><span data-stu-id="37231-109">For more information, see [Deleting a Rendering Context](deleting-a-rendering-context.md).</span></span> <span data-ttu-id="37231-110">Por último, tenga en cuenta que puede usar variables locales para los identificadores de contexto de dispositivo y de representación, ya que con las funciones [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) y [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) puede obtener identificadores para esos contextos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="37231-110">Finally, notice that you can use local variables for the device context and rendering context handles, because with the [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) and [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) functions you can obtain handles to those contexts as needed.</span></span>

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

 

 




