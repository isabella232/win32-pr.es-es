---
title: Cómo el cliente establece una conexión
description: Para establecer una sesión de comunicación cliente/servidor con un programa de servidor, las aplicaciones cliente con identificadores explícitos deben crear un identificador de enlace.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075839"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="e2eb2-103">Cómo el cliente establece una conexión</span><span class="sxs-lookup"><span data-stu-id="e2eb2-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="e2eb2-104">Para establecer una sesión de comunicación cliente/servidor con un programa de servidor, las aplicaciones cliente con identificadores explícitos deben crear un identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="e2eb2-105">Después de hacerlo, la biblioteca en tiempo de ejecución de RPC busca el equipo que hospeda el programa de servidor de.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="e2eb2-106">A continuación, busca el punto de conexión al que está escuchando el programa de servidor y dirige la llamada a él.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="e2eb2-107">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-107">The following diagram illustrates this process.</span></span>

![un cliente RPC establece una conexión con un servidor RPC](images/clntcon.png)

<span data-ttu-id="e2eb2-109">En esta sección se ofrece información acerca de cómo el cliente se conecta al programa de servidor y ejecuta los procedimientos remotos que ofrece.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="e2eb2-110">Existen muchos enfoques para completar estos pasos: en función del diseño elegido, una aplicación puede elegir un conjunto de pasos diferente.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="e2eb2-111">Este ejemplo es simplemente una forma de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e2eb2-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="e2eb2-112">La discusión se divide en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="e2eb2-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="e2eb2-113">Crear un controlador de enlace</span><span class="sxs-lookup"><span data-stu-id="e2eb2-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="e2eb2-114">Realización de una llamada a procedimiento remoto</span><span class="sxs-lookup"><span data-stu-id="e2eb2-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="e2eb2-115">Buscar el programa de servidor</span><span class="sxs-lookup"><span data-stu-id="e2eb2-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="e2eb2-116">Enviar la llamada al programa de servidor</span><span class="sxs-lookup"><span data-stu-id="e2eb2-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




