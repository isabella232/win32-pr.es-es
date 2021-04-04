---
title: Usar búferes de cadena
description: Las funciones que devuelven cadenas contienen un parámetro de entrada, Lpszbuffer se, y un parámetro de tamaño, lpdwBufferLength. Aunque Lpszbuffer se puede ser NULL, lpdwBufferLength debe ser un puntero válido a una variable DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792723"
---
# <a name="using-string-buffers"></a><span data-ttu-id="e465b-104">Usar búferes de cadena</span><span class="sxs-lookup"><span data-stu-id="e465b-104">Using String Buffers</span></span>

<span data-ttu-id="e465b-105">Las funciones que devuelven cadenas contienen un parámetro de entrada, *lpszbuffer se*, y un parámetro de tamaño, *lpdwBufferLength*.</span><span class="sxs-lookup"><span data-stu-id="e465b-105">Functions that return strings contain an input parameter, *lpszBuffer*, and a size parameter, *lpdwBufferLength*.</span></span> <span data-ttu-id="e465b-106">Aunque *lpszbuffer se* puede ser **null**, *lpdwBufferLength* debe ser un puntero válido a una variable **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e465b-106">Although *lpszBuffer* can be **NULL**, *lpdwBufferLength* must be a valid pointer to a **DWORD** variable.</span></span> <span data-ttu-id="e465b-107">Si el búfer de entrada al que apunta *lpszbuffer se* es **null** o demasiado pequeño para contener la cadena de salida, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="e465b-107">If the input buffer pointed to by *lpszBuffer* is **NULL** or too small to hold the output string, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="e465b-108">La variable a la que apunta *lpdwBufferLength* contiene un número que representa el número de bytes que requiere la función para devolver la cadena solicitada, incluido el terminador **null** .</span><span class="sxs-lookup"><span data-stu-id="e465b-108">The variable pointed to by *lpdwBufferLength* contains a number that represents the number of bytes the function requires to return the requested string, including the **null** terminator.</span></span> <span data-ttu-id="e465b-109">La aplicación debe asignar un búfer de este tamaño, establecer la variable a la que apunta *lpdwBufferLength* en este valor y volver a enviar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e465b-109">The application should allocate a buffer of this size, set the variable pointed to by *lpdwBufferLength* to this value, and resubmit the request.</span></span> <span data-ttu-id="e465b-110">Si el tamaño del búfer es suficiente para recibir la cadena solicitada, la cadena se copia en el búfer de salida con un terminador **null** y la función devuelve una indicación de éxito.</span><span class="sxs-lookup"><span data-stu-id="e465b-110">If the buffer size is sufficient to receive the requested string, the string is copied to the output buffer with a **null** terminator and the function returns a success indication.</span></span> <span data-ttu-id="e465b-111">La variable a la que apunta *lpdwBufferLength* ahora contiene el número de caracteres almacenados en el búfer, sin incluir el terminador **null** .</span><span class="sxs-lookup"><span data-stu-id="e465b-111">The variable pointed to by *lpdwBufferLength* now contains the number of characters stored in the buffer, excluding the **null** terminator.</span></span>

> [!Note]  
> <span data-ttu-id="e465b-112">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="e465b-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="e465b-113">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="e465b-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e465b-114">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e465b-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 