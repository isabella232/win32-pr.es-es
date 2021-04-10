---
title: Trasladar aplicaciones de sistema de ventana X
description: Trasladar aplicaciones de sistema de ventana X
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL en Windows, portabilidad
- trasladar a OpenGL, sistema de ventanas X
- Portabilidad de OpenGL, sistema X Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268872"
---
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="e6c49-106">Trasladar aplicaciones de sistema de ventana X</span><span class="sxs-lookup"><span data-stu-id="e6c49-106">Porting X Window System Applications</span></span>

<span data-ttu-id="e6c49-107">Al igual que Windows, el sistema de ventana X es un sistema basado en mensajes de control de eventos que usa controles de ventana y menús.</span><span class="sxs-lookup"><span data-stu-id="e6c49-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="e6c49-108">El código OpenGL de la aplicación X de la ventana del sistema se encuentra probablemente en áreas que se corresponden aproximadamente con el lugar en el que aparece cuando se traslada a Windows.</span><span class="sxs-lookup"><span data-stu-id="e6c49-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="e6c49-109">La mayoría del código OpenGL no cambiará, pero debe volver a escribir el código que sea específico del sistema X Window.</span><span class="sxs-lookup"><span data-stu-id="e6c49-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="e6c49-110">**Use el siguiente procedimiento general para trasladar los programas de OpenGL del sistema de ventana X a Windows**</span><span class="sxs-lookup"><span data-stu-id="e6c49-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="e6c49-111">Vuelva a escribir el código específico del sistema de la ventana X mediante código de Windows equivalente.</span><span class="sxs-lookup"><span data-stu-id="e6c49-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="e6c49-112">Busque la creación de ventanas y el código de control de eventos.</span><span class="sxs-lookup"><span data-stu-id="e6c49-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="e6c49-113">El sistema de ventana X y Windows son sistemas de ventanas basados en mensajes y de control de eventos, lo que facilita determinar dónde realizar los cambios adecuados.</span><span class="sxs-lookup"><span data-stu-id="e6c49-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="e6c49-114">(Sin embargo, especialmente en el caso de las aplicaciones de gran tamaño, la reescritura de una aplicación de un sistema operativo a otro puede ser una tarea compleja y difícil).</span><span class="sxs-lookup"><span data-stu-id="e6c49-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="e6c49-115">Busque cualquier código que use funciones GLX.</span><span class="sxs-lookup"><span data-stu-id="e6c49-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="e6c49-116">Estas son las funciones que traducirá a sus funciones equivalentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6c49-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="e6c49-117">Traduzca funciones de formato de píxel de GLX y funciones visuales/Dibujables al formato de píxeles Windows/OpenGL adecuado y a las funciones de contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6c49-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="e6c49-118">Traduzca funciones de contexto de representación de GLX a funciones de contexto de representación de Windows/OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e6c49-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="e6c49-119">Traduzca las funciones de GLX Pixmap a funciones equivalentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6c49-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="e6c49-120">Traduzca GLX fotogramas y otras funciones GLX a las funciones de Windows adecuadas.</span><span class="sxs-lookup"><span data-stu-id="e6c49-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




