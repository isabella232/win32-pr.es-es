---
title: Iniciar y detener el localizador de Microsoft
description: Las bibliotecas en tiempo de ejecución de RPC inician automáticamente el localizador de Microsoft cuando sea necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, tiene que borrar la base de datos durante la depuración de una aplicación distribuida.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075007"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="d9ed1-104">Iniciar y detener el localizador de Microsoft</span><span class="sxs-lookup"><span data-stu-id="d9ed1-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="d9ed1-105">Las bibliotecas en tiempo de ejecución de RPC inician automáticamente el localizador de Microsoft cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d9ed1-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="d9ed1-106">Puede detener e iniciar manualmente el localizador si, por ejemplo, tiene que borrar la base de datos durante la depuración de una aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="d9ed1-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="d9ed1-107">**Para detener e iniciar el localizador de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="d9ed1-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="d9ed1-108">En el panel de control, haga clic en el icono servicios.</span><span class="sxs-lookup"><span data-stu-id="d9ed1-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="d9ed1-109">Aparece el cuadro de diálogo **servicios** .</span><span class="sxs-lookup"><span data-stu-id="d9ed1-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="d9ed1-110">En el cuadro de diálogo **servicio** , seleccione **localizador de Microsoft** y, a continuación, haga clic en **iniciar** o **detener**.</span><span class="sxs-lookup"><span data-stu-id="d9ed1-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="d9ed1-111">También puede iniciar y detener el localizador de Microsoft desde la línea de comandos escribiendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d9ed1-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="d9ed1-112">**NET \[ Start/Stop \] rpclocator**</span><span class="sxs-lookup"><span data-stu-id="d9ed1-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="d9ed1-113">Solo un administrador puede iniciar el localizador de Microsoft una vez detenido.</span><span class="sxs-lookup"><span data-stu-id="d9ed1-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="d9ed1-114">Si se detiene, se reiniciará según las necesidades de las bibliotecas en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="d9ed1-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




