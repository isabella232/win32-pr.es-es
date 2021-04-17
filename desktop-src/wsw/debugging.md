---
title: Depurar (servicios Web de Windows)
description: Un conjunto de funciones solo está disponible en la compilación de depuración y está pensada para probar y depurar.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Depuración de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714517"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="adddb-106">Depurar (servicios Web de Windows)</span><span class="sxs-lookup"><span data-stu-id="adddb-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="adddb-107">Un conjunto de funciones solo está disponible en la compilación de depuración y está pensada para probar y depurar.</span><span class="sxs-lookup"><span data-stu-id="adddb-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="adddb-108">Solo hay una serie de funciones y variables de entorno disponibles en el modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="adddb-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="adddb-109">Se pueden usar para ayudar con las pruebas y la depuración.</span><span class="sxs-lookup"><span data-stu-id="adddb-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="adddb-110">Si se establece WsTimeout = 0, todos los tiempos de espera serán INFINITOs.</span><span class="sxs-lookup"><span data-stu-id="adddb-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="adddb-111">Esto resulta útil cuando se recorre el depurador durante las operaciones que dependen del tiempo.</span><span class="sxs-lookup"><span data-stu-id="adddb-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="adddb-112">Establecer WsFailCount tiene el mismo efecto que llamar a WsSetAutoFail.</span><span class="sxs-lookup"><span data-stu-id="adddb-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="adddb-113">WsFlags permite establecer varias marcas que modifican el comportamiento de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="adddb-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="adddb-114">La sintaxis es WsFlags = a, b, c.</span><span class="sxs-lookup"><span data-stu-id="adddb-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="adddb-115">Los marcadores admitidos son ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest y ModifySignatureValue.</span><span class="sxs-lookup"><span data-stu-id="adddb-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="adddb-116">Las siguientes funciones se usan con la depuración:</span><span class="sxs-lookup"><span data-stu-id="adddb-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="adddb-117">**WsDumpMemory**</span><span class="sxs-lookup"><span data-stu-id="adddb-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="adddb-118">**WsSetAutoFail**</span><span class="sxs-lookup"><span data-stu-id="adddb-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




