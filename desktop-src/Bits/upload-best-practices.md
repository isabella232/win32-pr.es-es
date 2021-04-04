---
title: Procedimientos recomendados de carga
description: Highloads puede provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a intentarlo.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075169"
---
# <a name="upload-best-practices"></a><span data-ttu-id="27b85-103">Procedimientos recomendados de carga</span><span class="sxs-lookup"><span data-stu-id="27b85-103">Upload Best Practices</span></span>

<span data-ttu-id="27b85-104">Highloads puede provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="27b85-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="27b85-105">Además, un gran número de conexiones pendientes consumirá más recursos del servidor y empeorará la situación.</span><span class="sxs-lookup"><span data-stu-id="27b85-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="27b85-106">Además, si la aplicación de back-end no se escribe para controlar las condiciones de carga elevada, puede bloquearse o provocar un comportamiento incorrecto.</span><span class="sxs-lookup"><span data-stu-id="27b85-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="27b85-107">La aplicación debe realizar los pasos siguientes para limitar la carga en el back-end.</span><span class="sxs-lookup"><span data-stu-id="27b85-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="27b85-108">Si no se escribe la aplicación de servidor para administrar grandes volúmenes, pueden producirse condiciones de tiempo de espera, lo que a su vez puede aumentar la carga cuando el cliente vuelve a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="27b85-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="27b85-109">Además, un gran número de conexiones pendientes consumirá más recursos del servidor.</span><span class="sxs-lookup"><span data-stu-id="27b85-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="27b85-110">Al probar la aplicación de servidor, pruebe con la carga más alta posible.</span><span class="sxs-lookup"><span data-stu-id="27b85-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="27b85-111">Debe usar varios equipos cliente, cada uno con varios trabajos de BITS simultáneos y de primer plano, y medir el rendimiento máximo en el back-end.</span><span class="sxs-lookup"><span data-stu-id="27b85-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="27b85-112">Si no puede medir el rendimiento, tendrá que calcular el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="27b85-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="27b85-113">La aplicación de servidor debe residir en una dirección URL diferente de la dirección URL de carga (vea la propiedad de IIS de BITS, **BITSServerNotificationURL**).</span><span class="sxs-lookup"><span data-stu-id="27b85-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="27b85-114">Se recomienda limitar la carga en el servidor de aplicaciones en función de los valores de rendimiento probados.</span><span class="sxs-lookup"><span data-stu-id="27b85-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="27b85-115">Debe utilizar las propiedades de IIS, **MaxBandwidth** y **MaxConnections**, para limitar la carga en el servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="27b85-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 




