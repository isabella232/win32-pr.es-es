---
title: Operaciones sincrónicas
description: Cuando se invoca RasDial como una operación sincrónica, la función no vuelve hasta que se ha establecido la conexión o se produce un error.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076206"
---
# <a name="synchronous-operations"></a><span data-ttu-id="5152b-103">Operaciones sincrónicas</span><span class="sxs-lookup"><span data-stu-id="5152b-103">Synchronous Operations</span></span>

<span data-ttu-id="5152b-104">Cuando se invoca [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) como una operación sincrónica, la función no vuelve hasta que se ha establecido la conexión o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="5152b-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="5152b-105">El modo sincrónico proporciona una manera sencilla para que un cliente RAS establezca una conexión.</span><span class="sxs-lookup"><span data-stu-id="5152b-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="5152b-106">El cliente puede llamar simplemente a **rasdial**, esperar a que se devuelva la función y, a continuación, llamar a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para determinar si la operación de conexión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5152b-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="5152b-107">Una vez establecida la conexión, la aplicación cliente puede finalizar sin interrumpir la conexión.</span><span class="sxs-lookup"><span data-stu-id="5152b-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="5152b-108">Si se produce un error, la aplicación cliente debe [cerrar la operación de conexión antes de](disconnecting.md) finalizar.</span><span class="sxs-lookup"><span data-stu-id="5152b-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="5152b-109">El inconveniente del modo sincrónico es que el cliente no recibe notificaciones de progreso a medida que la operación de conexión continúa.</span><span class="sxs-lookup"><span data-stu-id="5152b-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="5152b-110">Como solución alternativa para esta falta de notificaciones de progreso, un cliente en modo sincrónico puede usar un subproceso independiente que llama a [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para sondear y mostrar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="5152b-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="5152b-111">Sin embargo, para los clientes RAS que desean recibir información de progreso, la técnica preferida es invocar [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5152b-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




