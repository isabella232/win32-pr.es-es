---
description: En el ejemplo siguiente, el código de ensamblado de x86 obtiene el ID. de sesión de Terminal Services asociado al proceso actual.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obtener el ID. de sesión del proceso actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153035"
---
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="b6dc6-103">Obtener el ID. de sesión del proceso actual</span><span class="sxs-lookup"><span data-stu-id="b6dc6-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="b6dc6-104">\[Las direcciones de memoria especificadas por este código de ejemplo pueden cambiar en futuras versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="b6dc6-105">Para asegurarse de que la aplicación se siga ejecutando correctamente en el futuro, la aplicación debe llamar a [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) y, a continuación, a [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) en lugar de al siguiente código de ejemplo.\]</span><span class="sxs-lookup"><span data-stu-id="b6dc6-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="b6dc6-106">En el ejemplo siguiente, el código de ensamblado de x86 obtiene el ID. de sesión de Terminal Services asociado al proceso actual.</span><span class="sxs-lookup"><span data-stu-id="b6dc6-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
