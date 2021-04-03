---
title: Limpieza del lado servidor
description: Limpieza del lado servidor y llamada a procedimiento remoto (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075981"
---
# <a name="server-side-cleanup"></a><span data-ttu-id="46511-103">Limpieza del lado servidor</span><span class="sxs-lookup"><span data-stu-id="46511-103">Server-side Cleanup</span></span>

<span data-ttu-id="46511-104">Imagínese el siguiente escenario:</span><span class="sxs-lookup"><span data-stu-id="46511-104">Imagine the following scenario:</span></span>

<span data-ttu-id="46511-105">Un cliente abre un identificador de contexto y, a continuación, se detiene o pierde la conectividad con el servidor.</span><span class="sxs-lookup"><span data-stu-id="46511-105">A client opens a context handle, and then either stops or loses connectivity to the server.</span></span> <span data-ttu-id="46511-106">¿Cómo detecta el servidor que se ha producido un error en el cliente y se debe ejecutar el identificador de contexto?</span><span class="sxs-lookup"><span data-stu-id="46511-106">How does the server detect that the client has failed and the context handle should be run down?</span></span> <span data-ttu-id="46511-107">Hay dos subescenarios: uno es que el cliente se cierra de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="46511-107">There are two subscenarios: one is that the client is shut down in an orderly manner.</span></span> <span data-ttu-id="46511-108">En tal caso, notifica al servidor que se está cerrando y el servidor puede realizar la limpieza, incluida la realización de las ejecuciones de contexto.</span><span class="sxs-lookup"><span data-stu-id="46511-108">In such case, it notifies the server that it is shutting down, and the server can clean up, including performing context run downs.</span></span> <span data-ttu-id="46511-109">Si el cliente no se cierra de forma ordenada o no puede notificar al servidor, el servidor usa Keep alives para determinar si el cliente sigue estando disponible.</span><span class="sxs-lookup"><span data-stu-id="46511-109">If the client does not shut down in an orderly manner or it cannot notify the server, the server uses keep alives to determine whether the client is still available.</span></span> <span data-ttu-id="46511-110">En el lado del servidor, la función [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="46511-110">On the server side, the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function has no effect.</span></span> <span data-ttu-id="46511-111">En su lugar, el servidor usa la configuración global por máquina: Keep Alive, que tiene como valor predeterminado dos horas aproximadamente.</span><span class="sxs-lookup"><span data-stu-id="46511-111">Instead, the server uses the global per machine–keep alive setting, which defaults to approximately two hours.</span></span> <span data-ttu-id="46511-112">Si el cliente no responde a las conexiones de mantenimiento del servidor, la conexión está cerrada.</span><span class="sxs-lookup"><span data-stu-id="46511-112">If the client does not respond to the server's keep alives, the connection is closed.</span></span> <span data-ttu-id="46511-113">Cuando se cierran todas las conexiones a un proceso de cliente determinado, el servidor limpia y ejecuta los identificadores de contexto pendientes.</span><span class="sxs-lookup"><span data-stu-id="46511-113">When all connections to a given client process are closed, the server cleans up and runs down outstanding context handles.</span></span>

 

 




