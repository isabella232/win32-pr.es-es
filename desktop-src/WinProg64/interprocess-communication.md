---
title: Comunicación entre procesos
description: Las técnicas siguientes se pueden usar para la comunicación entre las aplicaciones de 32 bits y 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- 'comunicación entre procesos: programación de Windows de 64 bits'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421100"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="260b2-104">Comunicación entre procesos entre aplicaciones de 32 bits y de 64 bits</span><span class="sxs-lookup"><span data-stu-id="260b2-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="260b2-105">Las técnicas siguientes se pueden usar para la comunicación entre las aplicaciones de 32 bits y 64 bits:</span><span class="sxs-lookup"><span data-stu-id="260b2-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="260b2-106">las versiones de 64 bits de Windows usan identificadores de 32 bits para la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="260b2-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="260b2-107">Al compartir un controlador entre las aplicaciones de 32 bits y de 64 bits, solo los 32 bits inferiores son significativos, por lo que es seguro truncar el identificador (al pasarlo de 64 a 32 bits) o firmar el identificador (al pasarlo de 32 a 64 bits).</span><span class="sxs-lookup"><span data-stu-id="260b2-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="260b2-108">Entre los identificadores que se pueden compartir se incluyen los identificadores de los objetos de usuario como Windows (**hWnd**), los identificadores de objetos GDI, como lápices y pinceles (**hbrush** y **HPEN**), y los identificadores de objetos con nombre como exclusiones mutuas, semáforos e identificadores de archivo.</span><span class="sxs-lookup"><span data-stu-id="260b2-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="260b2-109">Se pueden utilizar llamadas a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="260b2-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="260b2-110">Los LocalServers COM se pueden usar si se registran archivos dll de proxy/stub de 32 bits y de 64 bits para todas las interfaces utilizadas.</span><span class="sxs-lookup"><span data-stu-id="260b2-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="260b2-111">Se puede utilizar la memoria compartida si los tipos dependientes del puntero se convierten correctamente (o se evitan).</span><span class="sxs-lookup"><span data-stu-id="260b2-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="260b2-112">Las funciones [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) y [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pueden iniciar procesos de 32 bits y de 64 bits desde procesos de 32 bits o de 64 bits con ciertas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="260b2-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="260b2-113">No se puede iniciar un archivo ejecutable de 64 bits ubicado en% WINDIR% \\ system32 desde un proceso de 32 bits, porque el redirector del sistema de archivos redirige la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="260b2-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="260b2-114">No deshabilite la redirección para lograr esto; Use% WINDIR% \\ Sysnative en su lugar.</span><span class="sxs-lookup"><span data-stu-id="260b2-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="260b2-115">Para obtener más información, consulte [redirector del sistema de archivos](file-system-redirector.md).</span><span class="sxs-lookup"><span data-stu-id="260b2-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 