---
title: Modelo de programación
description: En los primeros días de programación de equipos, cada programa se escribió como un fragmento monolítico grande, rellenado con instrucciones Goto.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776429"
---
# <a name="the-programming-model"></a><span data-ttu-id="086d0-103">Modelo de programación</span><span class="sxs-lookup"><span data-stu-id="086d0-103">The Programming Model</span></span>

<span data-ttu-id="086d0-104">En los primeros días de programación de equipos, cada programa se escribió como un fragmento monolítico grande, rellenado con instrucciones **goto** .</span><span class="sxs-lookup"><span data-stu-id="086d0-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="086d0-105">Cada programa tenía que administrar su propia entrada y salida en distintos dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="086d0-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="086d0-106">A medida que la disciplina de programación ha evolucionado, este código monolítico se organizó en procedimientos, con los procedimientos más usados empaquetados en bibliotecas para compartir y reutilizar.</span><span class="sxs-lookup"><span data-stu-id="086d0-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![instrucciones Goto monolíticas frente a procedimientos empaquetados en bibliotecas compartidas](images/prog-a06.png)

<span data-ttu-id="086d0-108">El lenguaje de programación C admite la programación orientada a procedimientos.</span><span class="sxs-lookup"><span data-stu-id="086d0-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="086d0-109">En C, el procedimiento principal se relaciona con todos los demás procedimientos como cuadros negros.</span><span class="sxs-lookup"><span data-stu-id="086d0-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="086d0-110">Por ejemplo, el procedimiento Main no puede averiguar cómo los procedimientos A, B y X realizan su trabajo.</span><span class="sxs-lookup"><span data-stu-id="086d0-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="086d0-111">El procedimiento Main solo llama a otro procedimiento; no tiene información sobre cómo se implementa el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="086d0-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![aislamiento de actividades realizadas en procedimientos externos](images/prog-a08.png)

<span data-ttu-id="086d0-113">Los lenguajes de programación orientados a procedimientos proporcionan mecanismos sencillos para especificar y escribir procedimientos.</span><span class="sxs-lookup"><span data-stu-id="086d0-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="086d0-114">Por ejemplo, el prototipo de función estándar de C de ANSI es una construcción que se usa para especificar el nombre de un procedimiento, el tipo del resultado que devuelve (si existe) y el número, la secuencia y el tipo de sus parámetros.</span><span class="sxs-lookup"><span data-stu-id="086d0-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="086d0-115">El uso del prototipo de función es una manera formal de especificar una interfaz entre los procedimientos.</span><span class="sxs-lookup"><span data-stu-id="086d0-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="086d0-116">Microsoft RPC se basa en ese modelo de programación, ya que permite que los procedimientos, agrupados en interfaces, residan en procesos diferentes a los del llamador.</span><span class="sxs-lookup"><span data-stu-id="086d0-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="086d0-117">Microsoft RPC también agrega un enfoque más formal a la definición de procedimiento que permite que el llamador y la rutina llamada adopten un contrato para intercambiar datos de forma remota e invocar la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="086d0-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="086d0-118">En el modelo de programación RPC de Microsoft, las llamadas de función tradicionales se complementan con dos elementos adicionales.</span><span class="sxs-lookup"><span data-stu-id="086d0-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="086d0-119">El primer elemento es un archivo. idl/. ACF que describe con precisión el intercambio de datos y el mecanismo de paso de parámetros entre el llamador y el procedimiento llamado.</span><span class="sxs-lookup"><span data-stu-id="086d0-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="086d0-120">El segundo elemento es un conjunto de API en tiempo de ejecución que proporcionan a los desarrolladores un control granular de la llamada a procedimiento remoto, incluidos los aspectos de seguridad, la administración del estado en el servidor, la especificación de qué clientes pueden comunicarse con el servidor, etc.</span><span class="sxs-lookup"><span data-stu-id="086d0-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




