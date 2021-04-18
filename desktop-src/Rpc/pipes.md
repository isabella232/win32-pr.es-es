---
title: Canalizaciones (RPC)
description: El constructor de tipo de canalización es un mecanismo muy eficaz para pasar grandes cantidades de datos o cualquier cantidad de datos que no esté disponible en la memoria al mismo tiempo.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC llamada a procedimiento remoto, descripción, canalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488765"
---
# <a name="pipes-rpc"></a><span data-ttu-id="e50f7-104">Canalizaciones (RPC)</span><span class="sxs-lookup"><span data-stu-id="e50f7-104">Pipes (RPC)</span></span>

<span data-ttu-id="e50f7-105">El constructor de tipo de canalización es un mecanismo muy eficaz para pasar grandes cantidades de datos o cualquier cantidad de datos que no esté disponible en la memoria al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e50f7-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="e50f7-106">Mediante el uso de una canalización, el tiempo de ejecución de RPC controla la transferencia de datos real, lo que elimina la sobrecarga asociada a llamadas a procedimiento remoto repetidas.</span><span class="sxs-lookup"><span data-stu-id="e50f7-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="e50f7-107">Una vez que un cliente invoca un procedimiento remoto que tiene un parámetro de canalización, el cliente y el servidor escriben bucles para transferir los datos.</span><span class="sxs-lookup"><span data-stu-id="e50f7-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="e50f7-108">Los datos se pueden producir en el cliente o el servidor.</span><span class="sxs-lookup"><span data-stu-id="e50f7-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="e50f7-109">En cualquier caso, no es necesario conocer la cantidad de datos (en bytes) de antemano.</span><span class="sxs-lookup"><span data-stu-id="e50f7-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="e50f7-110">Los datos se pueden generar o consumir incrementalmente.</span><span class="sxs-lookup"><span data-stu-id="e50f7-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="e50f7-111">En el bucle de transferencia de datos, el servidor llama a rutinas de código auxiliar que cargan o descargan un búfer de datos.</span><span class="sxs-lookup"><span data-stu-id="e50f7-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="e50f7-112">El cliente llama a los procedimientos definidos por el programador para asignar búferes, cargar datos en los búferes y descargarlos.</span><span class="sxs-lookup"><span data-stu-id="e50f7-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="e50f7-113">En esta sección se proporciona información general sobre el uso de canalizaciones para llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="e50f7-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="e50f7-114">Presenta la información general de los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e50f7-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="e50f7-115">Terminología de canalización esencial</span><span class="sxs-lookup"><span data-stu-id="e50f7-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="e50f7-116">El estado de la canalización</span><span class="sxs-lookup"><span data-stu-id="e50f7-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="e50f7-117">Definir canalizaciones en archivos IDL</span><span class="sxs-lookup"><span data-stu-id="e50f7-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="e50f7-118">Implementación de la canalización del lado cliente</span><span class="sxs-lookup"><span data-stu-id="e50f7-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="e50f7-119">Implementación de la canalización del lado servidor</span><span class="sxs-lookup"><span data-stu-id="e50f7-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="e50f7-120">Reglas para varias canalizaciones</span><span class="sxs-lookup"><span data-stu-id="e50f7-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="e50f7-121">Combinación de parámetros de canalización y no de canalización</span><span class="sxs-lookup"><span data-stu-id="e50f7-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="e50f7-122">Para obtener más información sobre la sintaxis de canalización y las restricciones, vea [canalización](/windows/desktop/Midl/pipe) en la referencia del lenguaje MIDL.</span><span class="sxs-lookup"><span data-stu-id="e50f7-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="e50f7-123">En el programa de ejemplo de CANALIZAciones del kit de desarrollo de software (SDK) de la plataforma \\ , el directorio RPC muestra cómo usar las canalizaciones **\[ in y out \]** para transferir datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="e50f7-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
