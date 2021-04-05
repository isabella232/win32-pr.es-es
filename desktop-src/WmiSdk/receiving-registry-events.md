---
description: El proveedor del registro del sistema intenta enviar una notificación para cada evento que se produce.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Recibir eventos del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082395"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="9d856-103">Recibir eventos del registro</span><span class="sxs-lookup"><span data-stu-id="9d856-103">Receiving Registry Events</span></span>

<span data-ttu-id="9d856-104">El proveedor del registro del sistema intenta enviar una notificación para cada evento que se produce.</span><span class="sxs-lookup"><span data-stu-id="9d856-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="9d856-105">Sin embargo, el proveedor del registro del sistema no garantiza que el consumidor reciba todos los eventos o todos ellos.</span><span class="sxs-lookup"><span data-stu-id="9d856-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="9d856-106">La excepción es que el proveedor del registro del sistema garantiza que un consumidor recibirá una notificación por cada registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d856-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="9d856-107">Por ejemplo, supongamos que un consumidor se registra para dos eventos de cambio de árbol y solicita una notificación para las instancias de [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) .</span><span class="sxs-lookup"><span data-stu-id="9d856-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="9d856-108">Cada registro tiene el mismo valor de Hive (subárbol) pero un valor de RootPath diferente.</span><span class="sxs-lookup"><span data-stu-id="9d856-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="9d856-109">Si las claves en ambas rutas cambian varias veces, el proveedor del registro del sistema garantiza que el consumidor recibirá una notificación para cada ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9d856-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="9d856-110">Dependiendo del tiempo de respuesta del registro y del proveedor del registro del sistema, el consumidor puede recibir tantas notificaciones como repeticiones de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d856-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d856-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d856-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d856-112">Registrar eventos del registro del sistema</span><span class="sxs-lookup"><span data-stu-id="9d856-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
