---
title: Cómo funciona RPC
description: Las herramientas de RPC hacen que parezcan los usuarios como si un cliente llama directamente a un procedimiento ubicado en un programa de servidor remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777370"
---
# <a name="how-rpc-works"></a><span data-ttu-id="5bfb5-103">Cómo funciona RPC</span><span class="sxs-lookup"><span data-stu-id="5bfb5-103">How RPC Works</span></span>

<span data-ttu-id="5bfb5-104">Las herramientas de RPC hacen que parezcan los usuarios como si un cliente llama directamente a un procedimiento ubicado en un programa de servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="5bfb5-105">El cliente y el servidor tienen sus propios espacios de direcciones. es decir, cada uno tiene su propio recurso de memoria asignado a los datos utilizados por el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="5bfb5-106">En la ilustración siguiente se muestra la arquitectura de RPC.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-106">The following figure illustrates the RPC architecture.</span></span>

![arquitectura de RPC](images/prog-a11.png)

<span data-ttu-id="5bfb5-108">Como se muestra en la ilustración, la aplicación cliente llama a un procedimiento de código auxiliar local en lugar de al código real que implementa el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="5bfb5-109">Los códigos auxiliares se compilan y vinculan con la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="5bfb5-110">En lugar de contener el código real que implementa el procedimiento remoto, el código auxiliar del cliente:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="5bfb5-111">Recupera los parámetros necesarios del espacio de direcciones del cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="5bfb5-112">Traduce los parámetros según sea necesario a un formato NDR estándar para su transmisión a través de la red.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="5bfb5-113">Llama a las funciones de la biblioteca en tiempo de ejecución del cliente RPC para enviar la solicitud y sus parámetros al servidor.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="5bfb5-114">El servidor realiza los pasos siguientes para llamar al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="5bfb5-115">Las funciones de la biblioteca en tiempo de ejecución RPC del servidor aceptan la solicitud y llaman al procedimiento de código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="5bfb5-116">El código auxiliar del servidor recupera los parámetros del búfer de red y los convierte del formato de transmisión de red al formato que el servidor necesita.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="5bfb5-117">El código auxiliar del servidor llama al procedimiento real en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="5bfb5-118">A continuación, se ejecuta el procedimiento remoto, lo que posiblemente genera parámetros de salida y un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="5bfb5-119">Una vez completado el procedimiento remoto, una secuencia similar de pasos devuelve los datos al cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="5bfb5-120">El procedimiento remoto devuelve sus datos al código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="5bfb5-121">El código auxiliar del servidor convierte los parámetros de salida en el formato necesario para la transmisión a través de la red y los devuelve a las funciones de la biblioteca en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="5bfb5-122">Las funciones de la biblioteca en tiempo de ejecución de RPC de servidor transmiten los datos de la red al equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="5bfb5-123">El cliente completa el proceso al aceptar los datos a través de la red y devolverlos a la función de llamada.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="5bfb5-124">La biblioteca en tiempo de ejecución de RPC del cliente recibe los valores devueltos del procedimiento remoto y los devuelve al código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="5bfb5-125">El código auxiliar del cliente convierte los datos de su NDR al formato utilizado por el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="5bfb5-126">El código auxiliar escribe datos en la memoria del cliente y devuelve el resultado al programa que realiza la llamada en el cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="5bfb5-127">El procedimiento de llamada continúa como si se hubiese llamado al procedimiento en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="5bfb5-128">Las bibliotecas en tiempo de ejecución se proporcionan en dos partes: una biblioteca de importación, que está vinculada a la aplicación y la biblioteca en tiempo de ejecución de RPC, que se implementa como una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="5bfb5-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="5bfb5-129">La aplicación de servidor contiene llamadas a las funciones de la biblioteca en tiempo de ejecución del servidor que registran la interfaz del servidor y permiten que el servidor acepte llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="5bfb5-130">La aplicación de servidor también contiene los procedimientos remotos específicos de la aplicación a los que llaman las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




