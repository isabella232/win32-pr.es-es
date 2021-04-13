---
title: Cómo se prepara el servidor para una conexión
description: Cuando se inicia la ejecución de un programa de servidor, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución de RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357259"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="ffc01-103">Cómo se prepara el servidor para una conexión</span><span class="sxs-lookup"><span data-stu-id="ffc01-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="ffc01-104">Cuando se inicia la ejecución de un programa de servidor, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="ffc01-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="ffc01-105">A continuación, crea la información de enlace necesaria.</span><span class="sxs-lookup"><span data-stu-id="ffc01-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="ffc01-106">El programa de servidor también debe registrar el punto de conexión o los puntos de conexión a los que escucha.</span><span class="sxs-lookup"><span data-stu-id="ffc01-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="ffc01-107">Después, puede empezar a escuchar las llamadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="ffc01-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="ffc01-108">Este proceso se ilustra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffc01-108">This process is illustrated in the following diagram.</span></span>

![una aplicación de servidor RPC se prepara para las conexiones de cliente](images/srvrcon.png)

<span data-ttu-id="ffc01-110">En función del diseño elegido, una aplicación de servidor puede elegir un conjunto diferente de pasos; en el ejemplo anterior y en la ilustración se ofrece un enfoque.</span><span class="sxs-lookup"><span data-stu-id="ffc01-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="ffc01-111">En esta sección se ofrece información acerca de los pasos que debe realizar un proceso de servidor para preparar una conexión.</span><span class="sxs-lookup"><span data-stu-id="ffc01-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="ffc01-112">La discusión se divide en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="ffc01-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="ffc01-113">Registrar la interfaz</span><span class="sxs-lookup"><span data-stu-id="ffc01-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="ffc01-114">Poner el servidor a disposición en la red</span><span class="sxs-lookup"><span data-stu-id="ffc01-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="ffc01-115">Registro de puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="ffc01-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="ffc01-116">Escuchando llamadas de cliente</span><span class="sxs-lookup"><span data-stu-id="ffc01-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




