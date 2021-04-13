---
title: Descargar un servidor con identificadores de contexto pendientes
description: Tradicionalmente, la descarga de un archivo DLL que atiende llamadas RPC con identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemática.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269296"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="84967-103">Descargar un servidor con identificadores de contexto pendientes</span><span class="sxs-lookup"><span data-stu-id="84967-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="84967-104">Tradicionalmente, la descarga de un archivo DLL que atiende llamadas RPC con identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemática.</span><span class="sxs-lookup"><span data-stu-id="84967-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="84967-105">Esto se debe a que la rutina de ejecución ya no es válida cuando se descarga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="84967-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="84967-106">Cuando se produce un error en un cliente con un identificador de contexto abierto previamente, y el tiempo de ejecución de RPC intenta cerrar el identificador de contexto, su intento de llamar al acceso a la rutina de ejecución infringe y el servidor se bloquea.</span><span class="sxs-lookup"><span data-stu-id="84967-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="84967-107">A partir de Windows XP, se ha agregado una nueva API denominada [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="84967-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="84967-108">**RpcServerUnregisterIfEx** cierra los identificadores de contexto abiertos por la interfaz que se va a eliminar del registro. la función [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) no lo hace.</span><span class="sxs-lookup"><span data-stu-id="84967-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="84967-109">El uso de **RpcServerUnregisterIfEx** no es necesario cuando se cierra todo el proceso, pero es necesario si se descargan uno o varios archivos DLL que hospedan las rutinas de ejecución mientras existan identificadores de contexto pendientes.</span><span class="sxs-lookup"><span data-stu-id="84967-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




