---
description: En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan algo.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceptos básicos de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155276"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="233f0-103">Conceptos básicos de autenticación</span><span class="sxs-lookup"><span data-stu-id="233f0-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="233f0-104">En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan algo.</span><span class="sxs-lookup"><span data-stu-id="233f0-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="233f0-105">Esto podría ser abrir y utilizar un archivo, tener acceso a un buzón, consultar una base de datos o imprimir un documento.</span><span class="sxs-lookup"><span data-stu-id="233f0-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="233f0-106">Los servidores son programas que proporcionan servicios a clientes como almacenamiento de archivos, control de correo, procesamiento de consultas y puesta en cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="233f0-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="233f0-107">Los clientes inician la acción, los servidores responden.</span><span class="sxs-lookup"><span data-stu-id="233f0-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="233f0-108">Normalmente, un servidor escucha en un puerto de comunicaciones en espera de que los clientes se conecten y soliciten el servicio.</span><span class="sxs-lookup"><span data-stu-id="233f0-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="233f0-109">En el modelo de protocolo Kerberos, cada conexión cliente/servidor comienza con la autenticación.</span><span class="sxs-lookup"><span data-stu-id="233f0-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="233f0-110">El cliente y el servidor, sucesivamente, ejecutan una serie de acciones diseñadas para garantizar a cada una de las partes de la conexión que la otra es auténtica.</span><span class="sxs-lookup"><span data-stu-id="233f0-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="233f0-111">Si la autenticación se lleva a cabo correctamente, la configuración de la sesión finalizará y se establecerá una sesión cliente/servidor segura.</span><span class="sxs-lookup"><span data-stu-id="233f0-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="233f0-112">El protocolo Kerberos hace uso de:</span><span class="sxs-lookup"><span data-stu-id="233f0-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="233f0-113">Autenticación de clave</span><span class="sxs-lookup"><span data-stu-id="233f0-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="233f0-114">Mensajes del autenticador</span><span class="sxs-lookup"><span data-stu-id="233f0-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="233f0-115">Distribución de claves</span><span class="sxs-lookup"><span data-stu-id="233f0-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="233f0-116">Vales de sesión</span><span class="sxs-lookup"><span data-stu-id="233f0-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="233f0-117">Vales de concesión de vales</span><span class="sxs-lookup"><span data-stu-id="233f0-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



