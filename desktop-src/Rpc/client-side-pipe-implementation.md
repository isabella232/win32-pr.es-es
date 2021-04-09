---
title: Implementación de Client-Side Pipe
description: Implementación de la canalización del lado cliente en llamada a procedimiento remoto (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903744"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="18594-103">Implementación de Client-Side Pipe</span><span class="sxs-lookup"><span data-stu-id="18594-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="18594-104">La aplicación cliente debe implementar los siguientes procedimientos, a los que llamará el código auxiliar de cliente durante la transferencia de datos:</span><span class="sxs-lookup"><span data-stu-id="18594-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="18594-105">Un procedimiento de extracción (para una canalización de entrada)</span><span class="sxs-lookup"><span data-stu-id="18594-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="18594-106">Un procedimiento de extracción (para una canalización de salida)</span><span class="sxs-lookup"><span data-stu-id="18594-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="18594-107">Un procedimiento de asignación para asignar un búfer para los datos de transferencia</span><span class="sxs-lookup"><span data-stu-id="18594-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="18594-108">Todos estos procedimientos deben usar los argumentos especificados por el archivo de encabezado generado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="18594-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="18594-109">Además, la aplicación cliente debe tener una variable de estado para identificar dónde ubicar o colocar los datos.</span><span class="sxs-lookup"><span data-stu-id="18594-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="18594-110">El procedimiento de asignación también puede ser tan simple o tan complejo como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="18594-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="18594-111">Por ejemplo, puede devolver un puntero al mismo búfer cada vez que el código auxiliar llama a la función, o puede asignar una cantidad de memoria diferente cada vez.</span><span class="sxs-lookup"><span data-stu-id="18594-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="18594-112">Si los datos ya tienen el formato adecuado (una matriz de elementos de canalización, por ejemplo), puede coordinar el procedimiento de asignación con el procedimiento de extracción para asignar un búfer que ya contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="18594-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="18594-113">En ese caso, el procedimiento de extracción puede ser una rutina vacía.</span><span class="sxs-lookup"><span data-stu-id="18594-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="18594-114">La asignación del búfer debe estar en bytes.</span><span class="sxs-lookup"><span data-stu-id="18594-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="18594-115">Los procedimientos de inserción y extracción, por otro lado, manipulan los elementos, cuyo tamaño en bytes depende de cómo se definieron.</span><span class="sxs-lookup"><span data-stu-id="18594-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="18594-116">En esta sección se describe la implementación del cliente de canalizaciones de entrada y salida en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="18594-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="18594-117">Implementar canalizaciones de entrada en el cliente</span><span class="sxs-lookup"><span data-stu-id="18594-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="18594-118">Implementar canalizaciones de salida en el cliente</span><span class="sxs-lookup"><span data-stu-id="18594-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




