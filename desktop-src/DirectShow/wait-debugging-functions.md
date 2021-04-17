---
description: Funciones de depuración de espera
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funciones de depuración de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687162"
---
# <a name="wait-debugging-functions"></a><span data-ttu-id="a6300-103">Funciones de depuración de espera</span><span class="sxs-lookup"><span data-stu-id="a6300-103">Wait Debugging Functions</span></span>

<span data-ttu-id="a6300-104">Microsoft DirectShow proporciona varias funciones para depurar las esperas infinitas.</span><span class="sxs-lookup"><span data-stu-id="a6300-104">Microsoft DirectShow provides several functions for debugging infinite waits.</span></span>

<span data-ttu-id="a6300-105">En las compilaciones comerciales, las funciones [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) y [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionan como sus homólogos de la API de Windows, **WaitForMultipleObjects** y **WaitForSingleObject**, con intervalos de tiempo de espera infinitos.</span><span class="sxs-lookup"><span data-stu-id="a6300-105">In retail builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions work like their Windows API counterparts, **WaitForMultipleObjects** and **WaitForSingleObject**, with infinite time-out intervals.</span></span>

<span data-ttu-id="a6300-106">En las compilaciones de depuración, estas funciones usan un valor de tiempo de espera global.</span><span class="sxs-lookup"><span data-stu-id="a6300-106">In debug builds, these functions use a global time-out value.</span></span> <span data-ttu-id="a6300-107">Si se agota el tiempo de espera, la función desencadena una aserción.</span><span class="sxs-lookup"><span data-stu-id="a6300-107">If the time-out expires, the function triggers an assert.</span></span> <span data-ttu-id="a6300-108">La siguiente clave del registro especifica el valor de tiempo de espera, en milisegundos:</span><span class="sxs-lookup"><span data-stu-id="a6300-108">The following registry key specifies the time-out value, in milliseconds:</span></span>

<span data-ttu-id="a6300-109">**HKEY \_ local \_ Machine \\ <DebugRoot> \\ <Module Name> \\ timeout**</span><span class="sxs-lookup"><span data-stu-id="a6300-109">**HKEY\_LOCAL\_MACHINE\\<DebugRoot>\\<Module Name>\\TIMEOUT**</span></span>

<span data-ttu-id="a6300-110">donde *<DebugRoot>* es la ruta de acceso del registro que se describe en el tema [depurar funciones de salida](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a6300-110">where *<DebugRoot>* is the registry path described in the topic [Debug Output Functions](debug-output-functions.md).</span></span>

<span data-ttu-id="a6300-111">Si la clave no existe, el valor predeterminado del tiempo de espera es infinito.</span><span class="sxs-lookup"><span data-stu-id="a6300-111">If the key does not exist, the time-out value defaults to INFINITE.</span></span> <span data-ttu-id="a6300-112">Puede usar la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para invalidar la entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="a6300-112">You can use the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function to override the registry entry.</span></span>



| <span data-ttu-id="a6300-113">Función</span><span class="sxs-lookup"><span data-stu-id="a6300-113">Function</span></span>                                                       | <span data-ttu-id="a6300-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6300-114">Description</span></span>                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="a6300-115">**DbgSetWaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="a6300-115">**DbgSetWaitTimeout**</span></span>](dbgsetwaittimeout.md)                 | <span data-ttu-id="a6300-116">Establece el valor de tiempo de espera de depuración.</span><span class="sxs-lookup"><span data-stu-id="a6300-116">Sets the debugging time-out value.</span></span>                              |
| [<span data-ttu-id="a6300-117">**DbgWaitForMultipleObjects**</span><span class="sxs-lookup"><span data-stu-id="a6300-117">**DbgWaitForMultipleObjects**</span></span>](dbgwaitformultipleobjects.md) | <span data-ttu-id="a6300-118">Espera a que se señalen todos los objetos especificados (o todos).</span><span class="sxs-lookup"><span data-stu-id="a6300-118">Waits for any (or all) of the specified objects to be signaled.</span></span> |
| [<span data-ttu-id="a6300-119">**DbgWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="a6300-119">**DbgWaitForSingleObject**</span></span>](dbgwaitforsingleobject.md)       | <span data-ttu-id="a6300-120">Espera a que se señale un objeto.</span><span class="sxs-lookup"><span data-stu-id="a6300-120">Waits for an object to become signaled.</span></span>                         |



 

 

 



