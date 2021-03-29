---
description: Cuando se produce una excepción en un proceso que se está depurando, el sistema notifica al depurador pasando la excepción a él. Esto se conoce como notificación de primera oportunidad. Después, el sistema suspende todos los subprocesos del proceso que se está depurando.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funciones de control de excepciones para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906924"
---
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="be906-105">Funciones de control de excepciones para la depuración</span><span class="sxs-lookup"><span data-stu-id="be906-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="be906-106">Cuando se produce una excepción en un proceso que se está depurando, el sistema notifica al depurador pasando la excepción a él.</span><span class="sxs-lookup"><span data-stu-id="be906-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="be906-107">Esto se conoce como *notificación de primera oportunidad*.</span><span class="sxs-lookup"><span data-stu-id="be906-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="be906-108">Después, el sistema suspende todos los subprocesos del proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="be906-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="be906-109">Si el depurador no controla la excepción, el sistema intenta encontrar un controlador de excepciones adecuado.</span><span class="sxs-lookup"><span data-stu-id="be906-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="be906-110">Si el sistema no encuentra uno adecuado, el sistema notifica de nuevo al depurador que se ha producido una excepción.</span><span class="sxs-lookup"><span data-stu-id="be906-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="be906-111">Esto se conoce como *notificación de última oportunidad*.</span><span class="sxs-lookup"><span data-stu-id="be906-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="be906-112">Si el depurador no controla la excepción después de la notificación de última oportunidad, el sistema finaliza el proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="be906-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="be906-113">Para obtener más información, vea [control de excepciones del depurador](debugger-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="be906-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



