---
description: Pseudoblocking las operaciones de pseudo bloqueo en Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo bloqueo y bloqueo real
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696810"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="9054c-103">Pseudo bloqueo y bloqueo real</span><span class="sxs-lookup"><span data-stu-id="9054c-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="9054c-104">En 16 entornos Windows, el sistema operativo no admite el bloqueo verdadero; por lo tanto, una operación de bloqueo que no se puede completar inmediatamente se administra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9054c-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="9054c-105">El proveedor de servicios inicia la operación y, a continuación, entra en un bucle durante el que envía los mensajes de Windows (lo que produce el procesador a otro subproceso si es necesario).</span><span class="sxs-lookup"><span data-stu-id="9054c-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="9054c-106">A continuación, comprueba la finalización de la función de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9054c-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="9054c-107">Si la función se ha completado, o si se ha invocado [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) , el bucle se termina y la función de bloqueo se completa con un resultado adecuado.</span><span class="sxs-lookup"><span data-stu-id="9054c-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="9054c-108">Esto es lo que se debe a la condición de pseudo bloqueo y el bucle al que se hace referencia anteriormente se conoce como el enlace de bloqueo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9054c-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
