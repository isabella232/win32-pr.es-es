---
description: Windows Sockets 2 sigue admitiendo todas las llamadas a funciones y semánticas de Windows Sockets 1,1, a excepción de las que se ocupan de los pseudo bloqueos.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problemas de compatibilidad de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275795"
---
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="37464-103">Problemas de compatibilidad de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="37464-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="37464-104">Windows Sockets 2 sigue admitiendo todas las llamadas a funciones y semánticas de Windows Sockets 1,1, a excepción de las que se ocupan de los pseudo bloqueos.</span><span class="sxs-lookup"><span data-stu-id="37464-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="37464-105">Dado que Windows Sockets 2 solo se ejecuta en entornos programados de 32 de forma preventiva, no es necesario implementar el pseudo bloqueo que se encuentra en Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="37464-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="37464-106">Esto significa que nunca se indicará el código de error WSAEINPROGRESS y que las siguientes funciones de Windows Sockets 1,1 no están disponibles para las aplicaciones de Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="37464-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="37464-107">WSACancelBlockingCall</span><span class="sxs-lookup"><span data-stu-id="37464-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="37464-108">WSAIsBlocking</span><span class="sxs-lookup"><span data-stu-id="37464-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="37464-109">WSASetBlockingHook</span><span class="sxs-lookup"><span data-stu-id="37464-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="37464-110">WSAUnhookBlockingHook</span><span class="sxs-lookup"><span data-stu-id="37464-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="37464-111">Los programas de Windows Sockets 1,1 que se escriben para utilizar el pseudo-bloqueo seguirán funcionando correctamente, ya que se vinculan a Winsock.dll o Wsock32.dll.</span><span class="sxs-lookup"><span data-stu-id="37464-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="37464-112">Ambos continúan admitiendo el conjunto completo de funciones 1,1 de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="37464-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="37464-113">Para que los programas se conviertan en aplicaciones de Windows Sockets 2, se debe modificar el código.</span><span class="sxs-lookup"><span data-stu-id="37464-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="37464-114">En la mayoría de los casos, el uso prudente de los subprocesos se puede sustituir para acomodar el procesamiento que se estaba llevando a cabo con una función de enlace de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="37464-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 



