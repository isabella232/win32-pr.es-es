---
title: Paquetes de respuesta de BITS
description: Paquetes de respuesta de BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903144"
---
# <a name="bits-response-packets"></a><span data-ttu-id="d5659-103">Paquetes de respuesta de BITS</span><span class="sxs-lookup"><span data-stu-id="d5659-103">BITS Response Packets</span></span>

<span data-ttu-id="d5659-104">En la tabla siguiente se enumeran los paquetes de respuesta enviados al cliente de BITS para los trabajos de carga y de carga y respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5659-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="d5659-105">En la tabla se enumeran los paquetes en la secuencia típica que se envían al cliente.</span><span class="sxs-lookup"><span data-stu-id="d5659-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="d5659-106">Paquete de respuesta</span><span class="sxs-lookup"><span data-stu-id="d5659-106">Response packet</span></span>                                      | <span data-ttu-id="d5659-107">Propósito</span><span class="sxs-lookup"><span data-stu-id="d5659-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5659-108">Confirmación del ping</span><span class="sxs-lookup"><span data-stu-id="d5659-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="d5659-109">Confirma la solicitud de [ping](ping.md) .</span><span class="sxs-lookup"><span data-stu-id="d5659-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="d5659-110">Confirmación de creación: sesión</span><span class="sxs-lookup"><span data-stu-id="d5659-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="d5659-111">Confirma la solicitud [de creación de sesión](create-session.md) y devuelve un identificador de sesión que el cliente de bits usa en todas las solicitudes posteriores para identificar esta sesión de transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="d5659-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="d5659-112">Confirmación para fragmento</span><span class="sxs-lookup"><span data-stu-id="d5659-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="d5659-113">Confirma la solicitud de [fragmento](fragment.md) y escribe el fragmento en el archivo de carga en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d5659-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="d5659-114">Confirmación de cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="d5659-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="d5659-115">Confirma la solicitud [de cierre de sesión](close-session.md) y libera todos los recursos asociados a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d5659-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="d5659-116">Confirmación para cancelar sesión</span><span class="sxs-lookup"><span data-stu-id="d5659-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="d5659-117">Confirma la solicitud [de cancelación de sesión](cancel-session.md) y libera todos los recursos asociados a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d5659-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




