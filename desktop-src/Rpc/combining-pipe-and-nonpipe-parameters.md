---
title: Combinación de parámetros de canalización y no de canalización
description: Combinación de parámetros de canalización y no de canalización en llamada a procedimiento remoto (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904751"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="5d005-103">Combinación de parámetros de canalización y no de canalización</span><span class="sxs-lookup"><span data-stu-id="5d005-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="5d005-104">Cuando se combinan tipos de canalización y otros tipos en una llamada a procedimiento remoto, los datos se transmiten según la dirección del parámetro:</span><span class="sxs-lookup"><span data-stu-id="5d005-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="5d005-105">En la **\[ \] dirección,** los datos de todos los argumentos que no son de canalización se transmiten primero, seguidos de los datos de canalización.</span><span class="sxs-lookup"><span data-stu-id="5d005-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="5d005-106">En la dirección de **\[ salida \]** , el servidor envía los datos de la canalización en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="5d005-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="5d005-107">Una vez que la rutina de administrador devuelve, el servidor transmite los datos no canalizados.</span><span class="sxs-lookup"><span data-stu-id="5d005-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="5d005-108">Cuando hay **\[ en, \]** los argumentos out Pipe combinados con argumentos **\[ in, \] out** sin canalización, primero se transmiten los datos de entrada en su totalidad, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5d005-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="5d005-109">A continuación, los datos de salida se transmiten como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5d005-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="5d005-110">La siguiente restricción se aplica a esta implementación de canalizaciones (MIDL 3,0): cuando se combinan tipos de canalización y otros tipos en una única llamada a procedimiento remoto, los parámetros no de canalización deben tener un tamaño bien definido para permitir que el compilador de MIDL calcule el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="5d005-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="5d005-111">Por ejemplo, no puede combinar parámetros de canalización con un \[ puntero [único](/windows/desktop/Midl/unique) \] o una estructura conforme, ya que sus tamaños no se pueden determinar en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="5d005-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d005-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d005-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d005-113">codo</span><span class="sxs-lookup"><span data-stu-id="5d005-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="5d005-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="5d005-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 