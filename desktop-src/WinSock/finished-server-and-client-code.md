---
description: Ejecutar el código de ejemplo completo de la aplicación de servidor y cliente TCP/IP.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Ejecución del ejemplo de código de servidor y cliente Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001143"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="af23e-103">Ejecución del ejemplo de código de servidor y cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="af23e-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="af23e-104">Esta sección contiene el código fuente completo de las aplicaciones de cliente y servidor de TCP/IP:</span><span class="sxs-lookup"><span data-stu-id="af23e-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="af23e-105">Completar el código de cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="af23e-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="af23e-106">Completar el código del servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="af23e-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="af23e-107">La aplicación de servidor debe iniciarse antes de que se inicie la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="af23e-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="af23e-108">Para ejecutar el servidor, compile el código fuente completo del servidor y ejecute el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="af23e-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="af23e-109">La aplicación de servidor escucha en el puerto TCP 27015 para que un cliente se conecte.</span><span class="sxs-lookup"><span data-stu-id="af23e-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="af23e-110">Una vez que un cliente se conecta, el servidor recibe datos del cliente y repite (envía) los datos recibidos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="af23e-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="af23e-111">Cuando el cliente cierra la conexión, el servidor apaga el socket de cliente, cierra el socket y se cierra.</span><span class="sxs-lookup"><span data-stu-id="af23e-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="af23e-112">Para ejecutar el cliente, compile el código fuente completo del cliente y ejecute el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="af23e-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="af23e-113">La aplicación cliente requiere que el nombre del equipo o la dirección IP del equipo en el que se ejecuta la aplicación de servidor se pase como un parámetro de línea de comandos cuando se ejecute el cliente.</span><span class="sxs-lookup"><span data-stu-id="af23e-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="af23e-114">Si el cliente y el servidor se ejecutan en el equipo de ejemplo, el cliente se puede iniciar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="af23e-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="af23e-115">**localhost de cliente**</span><span class="sxs-lookup"><span data-stu-id="af23e-115">**client localhost**</span></span>

<span data-ttu-id="af23e-116">El cliente intenta conectarse al servidor en el puerto TCP 27015.</span><span class="sxs-lookup"><span data-stu-id="af23e-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="af23e-117">Una vez que el cliente se conecta, el cliente envía datos al servidor y recibe los datos devueltos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="af23e-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="af23e-118">Después, el cliente cierra el socket y se cierra.</span><span class="sxs-lookup"><span data-stu-id="af23e-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af23e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af23e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af23e-120">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="af23e-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



