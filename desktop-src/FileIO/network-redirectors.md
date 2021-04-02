---
description: Describe la funcionalidad de un redirector de red.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirectores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913533"
---
# <a name="network-redirectors"></a><span data-ttu-id="59be7-103">Redirectores de red</span><span class="sxs-lookup"><span data-stu-id="59be7-103">Network Redirectors</span></span>

<span data-ttu-id="59be7-104">Un redirector de red es un controlador del sistema de archivos (o FSD) que funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="59be7-104">A network redirector is a file system driver (or FSD) that functions in the following manner:</span></span>

-   <span data-ttu-id="59be7-105">Como cliente en una operación de e/s de red mediante el envío de solicitudes de e/s a los servidores y el procesamiento de las respuestas de los servidores.</span><span class="sxs-lookup"><span data-stu-id="59be7-105">As a client in a network I/O operation by sending I/O requests to servers and processing the responses from the servers.</span></span>
-   <span data-ttu-id="59be7-106">Como servidor en una operación de e/s de red mediante la recepción de solicitudes de e/s de los servidores y el procesamiento de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="59be7-106">As a server in a network I/O operation by receiving I/O requests from servers and processing the requests.</span></span>

<span data-ttu-id="59be7-107">Realiza toda la interacción de bajo nivel con el servidor para resolver el nombre de archivo proporcionado por la aplicación con la ubicación del recurso en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="59be7-107">It performs all of the low-level interaction with the server in resolving the file name provided by the application with the location of the resource on the remote server.</span></span> <span data-ttu-id="59be7-108">De esta manera, el redirector permite a la aplicación tener acceso a los recursos de los servidores remotos y manipularlos como si se encontraran en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="59be7-108">In this way, the redirector enables the application to access and manipulate resources on remote servers as if they were located on the local machine.</span></span>

<span data-ttu-id="59be7-109">Los redirectores funcionan completamente dentro del modo kernel.</span><span class="sxs-lookup"><span data-stu-id="59be7-109">Redirectors operate entirely within kernel mode.</span></span> <span data-ttu-id="59be7-110">Esto proporciona las siguientes ventajas de rendimiento frente a las alternativas de modo de usuario:</span><span class="sxs-lookup"><span data-stu-id="59be7-110">This provides the following performance advantages over user-mode alternatives:</span></span>

-   <span data-ttu-id="59be7-111">Puede interactuar con FSDs en modo kernel que se ejecuta en el servidor, como el servidor FSD, sin necesidad de los cambios de contexto del modo de usuario a kernel y del modo de kernel a usuario.</span><span class="sxs-lookup"><span data-stu-id="59be7-111">It can interact with kernel-mode FSDs running on the server, such as the server FSD, without the need for user-to-kernel mode and kernel-to-user mode context switches.</span></span>
-   <span data-ttu-id="59be7-112">Puede interactuar en modo kernel con el administrador de caché en el servidor para almacenar en caché los datos de e/s que el administrador de caché del servidor envía en el cliente.</span><span class="sxs-lookup"><span data-stu-id="59be7-112">It can interact in kernel mode with the cache manager on the server to cache I/O data that the server cache manager sends on the client.</span></span>
-   <span data-ttu-id="59be7-113">Las funciones de API personalizadas para las solicitudes de e/s remotas y los cambios en las funciones de e/s de archivos estándar para proporcionar esta funcionalidad no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="59be7-113">API functions custom-made for remote I/O requests, and changes to the standard file I/O functions to provide this functionality, are not necessary.</span></span>

 

 



