---
description: Un buzón de correo es un pseudofile que reside en la memoria y utiliza funciones de archivo estándar para tener acceso a él.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Acerca de los procesadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669963"
---
# <a name="about-mailslots"></a><span data-ttu-id="0bde0-103">Acerca de los procesadores</span><span class="sxs-lookup"><span data-stu-id="0bde0-103">About Mailslots</span></span>

<span data-ttu-id="0bde0-104">Un buzón de correo es un pseudofile que reside en la memoria y utiliza funciones de archivo estándar para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="0bde0-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="0bde0-105">Los datos de un mensaje de buzón de correo pueden estar en cualquier formato, pero no pueden ser mayores de 424 bytes cuando se envían entre equipos.</span><span class="sxs-lookup"><span data-stu-id="0bde0-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="0bde0-106">A diferencia de los archivos de disco, los buzones de archivos son temporales.</span><span class="sxs-lookup"><span data-stu-id="0bde0-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="0bde0-107">Cuando se cierran todos los identificadores de un buzón de correo, el buzón de correo y todos los datos que contiene se eliminan.</span><span class="sxs-lookup"><span data-stu-id="0bde0-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="0bde0-108">Un *servidor de buzón de correo* es un proceso que crea y posee un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0bde0-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="0bde0-109">Cuando el servidor crea un buzón de correo, recibe un identificador de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0bde0-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="0bde0-110">Este identificador se debe utilizar cuando un proceso Lee los mensajes del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0bde0-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="0bde0-111">Solo el proceso que crea un buzón de correo o que ha obtenido el identificador de otro mecanismo (como la herencia) puede leer desde el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0bde0-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="0bde0-112">Todos los procesadores de curso son locales para el proceso que los crea.</span><span class="sxs-lookup"><span data-stu-id="0bde0-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="0bde0-113">Un proceso no puede crear un buzón remoto.</span><span class="sxs-lookup"><span data-stu-id="0bde0-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="0bde0-114">Un *cliente de buzón de correo* es un proceso que escribe un mensaje en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0bde0-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="0bde0-115">Cualquier proceso que tenga el nombre de un buzón de correo puede colocar un mensaje allí.</span><span class="sxs-lookup"><span data-stu-id="0bde0-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="0bde0-116">Los mensajes nuevos siguen los mensajes existentes en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0bde0-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="0bde0-117">Los procesadores de mensajes pueden difundir mensajes dentro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="0bde0-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="0bde0-118">Si cada uno de los procesos de un dominio crea un buzón de correo con el mismo nombre, los procesos participantes reciben todos los mensajes que se dirigen a ese buzón de correo y se envían al dominio.</span><span class="sxs-lookup"><span data-stu-id="0bde0-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="0bde0-119">Dado que un proceso puede controlar un identificador de buzón de correo de servidor y el identificador de cliente recuperados cuando se abre el buzón de correo para una operación de escritura, las aplicaciones pueden implementar fácilmente una sencilla característica de paso de mensajes dentro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="0bde0-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="0bde0-120">Para enviar mensajes de más de 424 bytes entre equipos, utilice [canalizaciones con nombre](named-pipes.md) o [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0bde0-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bde0-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bde0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bde0-122">Nombres de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="0bde0-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="0bde0-123">Operaciones de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="0bde0-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
