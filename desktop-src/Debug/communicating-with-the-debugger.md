---
description: La función OutputDebugString envía una cadena desde el proceso que se está depurando al depurador generando un evento de depuración de \_ eventos de cadena de depuración de salida \_ \_ . Un proceso puede detectar si se está depurando llamando a la función IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicarse con el depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906932"
---
# <a name="communicating-with-the-debugger"></a><span data-ttu-id="7ba67-104">Comunicarse con el depurador</span><span class="sxs-lookup"><span data-stu-id="7ba67-104">Communicating with the Debugger</span></span>

<span data-ttu-id="7ba67-105">La función [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envía una cadena desde el proceso que se está depurando al depurador generando un evento de depuración de \_ eventos de cadena de depuración de salida \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7ba67-105">The [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) function sends a string from the process being debugged to the debugger by generating an OUTPUT\_DEBUG\_STRING\_EVENT debugging event.</span></span> <span data-ttu-id="7ba67-106">Un proceso puede detectar si se está depurando llamando a la función [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="7ba67-106">A process can detect whether it is being debugged by calling the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>

<span data-ttu-id="7ba67-107">La función [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) produce una excepción de punto de interrupción en el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="7ba67-107">The [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function causes a breakpoint exception in the current process.</span></span> <span data-ttu-id="7ba67-108">Un punto de interrupción es una ubicación en un programa donde la ejecución se detiene para permitir al desarrollador examinar el código, las variables y los valores de registro del programa y, si es necesario, realizar cambios, continuar la ejecución o finalizar la ejecución.</span><span class="sxs-lookup"><span data-stu-id="7ba67-108">A breakpoint is a location in a program where execution is stopped to allow the developer to examine the program's code, variables, and register values and, as necessary, to make changes, continue execution, or terminate execution.</span></span>

<span data-ttu-id="7ba67-109">La función [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) finaliza el proceso actual y proporciona el control de ejecución al depurador, pero a diferencia de [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), no genera una excepción.</span><span class="sxs-lookup"><span data-stu-id="7ba67-109">The [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) function terminates the current process and gives execution control to the debugger, but unlike [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), it does not generate an exception.</span></span> <span data-ttu-id="7ba67-110">Esta función solo se debe usar como último recurso, ya que no siempre libera la memoria del proceso ni cierra sus archivos.</span><span class="sxs-lookup"><span data-stu-id="7ba67-110">This function should only be used as a last resort, because it does not always free the process's memory or close its files.</span></span>

 

 
