---
title: Prácticas recomendadas de WinRM
description: En este tema se explican algunas de las prácticas recomendadas para usar las distintas características de la API de WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995307"
---
# <a name="winrm-best-practices"></a><span data-ttu-id="3535e-103">Prácticas recomendadas de WinRM</span><span class="sxs-lookup"><span data-stu-id="3535e-103">WinRM Best Practices</span></span>

<span data-ttu-id="3535e-104">En este tema se explican algunas de las prácticas recomendadas para usar las distintas características de la API de WinRM.</span><span class="sxs-lookup"><span data-stu-id="3535e-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="3535e-105">Cuotas</span><span class="sxs-lookup"><span data-stu-id="3535e-105">Quotas</span></span>

<span data-ttu-id="3535e-106">Cuando se alcanza una cuota, el servicio WinRM devuelve un error al cliente.</span><span class="sxs-lookup"><span data-stu-id="3535e-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="3535e-107">Como resultado, la lógica del cliente debe reintentar explícitamente la operación según el error devuelto.</span><span class="sxs-lookup"><span data-stu-id="3535e-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="3535e-108">Suscripciones a eventos</span><span class="sxs-lookup"><span data-stu-id="3535e-108">Event subscriptions</span></span>

<span data-ttu-id="3535e-109">Al usar suscripciones iniciadas por el recopilador, limite el número de equipos remotos a 500 y aísle el servicio [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) en un proceso de host independiente.</span><span class="sxs-lookup"><span data-stu-id="3535e-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="3535e-110">Un error de conexión contendrá un subproceso hasta que se agote el tiempo de espera. Un gran número de errores de conexión simultáneos puede provocar el agotamiento del grupo de subprocesos y dejar que el servidor deje de responder.</span><span class="sxs-lookup"><span data-stu-id="3535e-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 