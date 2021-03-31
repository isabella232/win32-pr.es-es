---
title: Operaciones asincrónicas
description: Cuando se invoca RasDial como una operación asincrónica, la función vuelve inmediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418815"
---
# <a name="asynchronous-operations"></a><span data-ttu-id="89eec-103">Operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="89eec-103">Asynchronous Operations</span></span>

<span data-ttu-id="89eec-104">Cuando se invoca [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) como una operación asincrónica, la función vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="89eec-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as an asynchronous operation, the function returns immediately.</span></span> <span data-ttu-id="89eec-105">En el modo asincrónico, la llamada **rasdial** debe especificar un [controlador de notificación](notification-handlers.md) que el administrador de conexiones de acceso remoto utiliza para informar al cliente siempre que la operación de conexión cambie de estado o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="89eec-105">In asynchronous mode, the **RasDial** call must specify a [notification handler](notification-handlers.md) that the Remote Access Connection Manager uses to inform the client whenever the connection operation changes states or an error occurs.</span></span>

<span data-ttu-id="89eec-106">El controlador de notificación puede ser una ventana para recibir mensajes o una función de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)o [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) .</span><span class="sxs-lookup"><span data-stu-id="89eec-106">The notification handler can be a window to receive messages, or a [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1), or [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) callback function.</span></span> <span data-ttu-id="89eec-107">El administrador de conexiones de acceso remoto realiza sus notificaciones asincrónicas en el contexto del subproceso que realizó la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .</span><span class="sxs-lookup"><span data-stu-id="89eec-107">The Remote Access Connection Manager makes its asynchronous notifications in the context of the thread that made the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span> <span data-ttu-id="89eec-108">Por esta razón, el subproceso que realiza la llamada no debe finalizar hasta que la operación de conexión se haya establecido correctamente o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="89eec-108">For this reason, the calling thread must not terminate until the connection operation has been successfully established or an error occurs.</span></span> <span data-ttu-id="89eec-109">Como en modo sincrónico, la aplicación cliente puede terminar con seguridad una vez que se ha establecido la conexión y debe [cerrar la operación de conexión](disconnecting.md) si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="89eec-109">As in synchronous mode, the client application can safely terminate once the connection has been established, and it must [shut down the connection operation](disconnecting.md) if an error occurs.</span></span>

 

 




