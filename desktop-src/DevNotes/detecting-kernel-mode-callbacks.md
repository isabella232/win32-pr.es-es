---
description: Si un subproceso está esperando a que se complete una devolución de llamada de modo kernel, el lado del modo de usuario del subproceso retrasará en una llamada a la función ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Detección de devoluciones de llamada de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000708"
---
# <a name="detecting-kernel-mode-callbacks"></a><span data-ttu-id="effdd-103">Detección de devoluciones de llamada de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="effdd-103">Detecting Kernel-Mode Callbacks</span></span>

<span data-ttu-id="effdd-104">La mayor parte del código para el sistema operativo Windows se ejecuta en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="effdd-104">Most of the code for the Windows operating system runs in kernel mode.</span></span> <span data-ttu-id="effdd-105">El modo de procesador cambia del modo de usuario al modo kernel siempre que un subproceso de aplicación llama a una función de la API de Windows que, a su vez, llama a una función del sistema interna que debe ejecutarse en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="effdd-105">The processor mode switches from user mode to kernel mode whenever an application thread calls a function from the Windows API that in turn calls an internal system function that must execute in kernel mode.</span></span> <span data-ttu-id="effdd-106">El modo de procesador vuelve al modo de usuario antes de que el control vuelva a la función de modo que los datos del sistema estén protegidos.</span><span class="sxs-lookup"><span data-stu-id="effdd-106">The processor mode returns to user mode before control returns to the function so that the system data is protected.</span></span>

<span data-ttu-id="effdd-107">Si un subproceso está esperando a que se complete una devolución de llamada de modo kernel, el lado del modo de usuario del subproceso retrasará en una llamada a la función **ZwCallbackReturn** .</span><span class="sxs-lookup"><span data-stu-id="effdd-107">If a thread is waiting for a kernel-mode callback to complete, the user-mode side of the thread will delay at a call to the **ZwCallbackReturn** function.</span></span>

 

 



