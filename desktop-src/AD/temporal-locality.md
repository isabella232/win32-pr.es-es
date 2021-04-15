---
title: Localidad temporal
description: La localidad temporal es una estrategia de prevención que reduce la ventana para las actualizaciones parciales.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486579"
---
# <a name="temporal-locality"></a><span data-ttu-id="03ba4-103">Localidad temporal</span><span class="sxs-lookup"><span data-stu-id="03ba4-103">Temporal Locality</span></span>

<span data-ttu-id="03ba4-104">La *localidad temporal* es una estrategia de prevención que reduce la ventana para las actualizaciones parciales.</span><span class="sxs-lookup"><span data-stu-id="03ba4-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="03ba4-105">La replicación de los cambios de una réplica de origen determinada continúa en orden USN ascendente.</span><span class="sxs-lookup"><span data-stu-id="03ba4-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="03ba4-106">Las escrituras que se producen juntas en el tiempo tendrán los USN "cercanos" entre sí y se propagarán cerca del tiempo.</span><span class="sxs-lookup"><span data-stu-id="03ba4-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="03ba4-107">Las aplicaciones que crean o actualizan varios objetos relacionados deben escribir los objetos lo más cerca posible del tiempo.</span><span class="sxs-lookup"><span data-stu-id="03ba4-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="03ba4-108">Por ejemplo, la aplicación podría recopilar toda la información necesaria del usuario y aplicarla al directorio cuando el usuario haga clic en un botón "aplicar".</span><span class="sxs-lookup"><span data-stu-id="03ba4-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="03ba4-109">La localidad temporal también reduce la probabilidad de que se produzca una resolución de colisiones introduciendo incoherencias dentro de los objetos.</span><span class="sxs-lookup"><span data-stu-id="03ba4-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




