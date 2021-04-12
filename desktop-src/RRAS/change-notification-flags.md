---
title: Cambiar marcas de notificación
description: Cambiar marcas de notificación
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Cambio
- Cambiar marcas de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357176"
---
# <a name="change-notification-flags"></a><span data-ttu-id="26dc0-105">Cambiar marcas de notificación</span><span class="sxs-lookup"><span data-stu-id="26dc0-105">Change Notification Flags</span></span>



| <span data-ttu-id="26dc0-106">Constante</span><span class="sxs-lookup"><span data-stu-id="26dc0-106">Constant</span></span>                         | <span data-ttu-id="26dc0-107">Value</span><span class="sxs-lookup"><span data-stu-id="26dc0-107">Value</span></span>      | <span data-ttu-id="26dc0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="26dc0-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26dc0-109">\_tipos de \_ cambio de número RTM \_</span><span class="sxs-lookup"><span data-stu-id="26dc0-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="26dc0-110">3</span><span class="sxs-lookup"><span data-stu-id="26dc0-110">3</span></span>          | <span data-ttu-id="26dc0-111">Especifica el número de tipos de cambios utilizados actualmente por el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="26dc0-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="26dc0-112">tipo de cambio de RTM \_ \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="26dc0-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="26dc0-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="26dc0-113">0x0001</span></span>     | <span data-ttu-id="26dc0-114">Notifica al cliente cualquier cambio que se haya efectuado en un destino.</span><span class="sxs-lookup"><span data-stu-id="26dc0-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="26dc0-115">tipo de cambio de RTM \_ \_ \_ mejor</span><span class="sxs-lookup"><span data-stu-id="26dc0-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="26dc0-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="26dc0-116">0x0002</span></span>     | <span data-ttu-id="26dc0-117">Notifica al cliente los cambios en la mejor ruta o cuando cambia la mejor ruta.</span><span class="sxs-lookup"><span data-stu-id="26dc0-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="26dc0-118">\_cambio de \_ \_ reenvío de tipos de RTM</span><span class="sxs-lookup"><span data-stu-id="26dc0-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="26dc0-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="26dc0-119">0x0004</span></span>     | <span data-ttu-id="26dc0-120">Notifica al cliente los cambios de ruta más adecuados que afectan al reenvío (por ejemplo, los cambios en el próximo salto).</span><span class="sxs-lookup"><span data-stu-id="26dc0-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="26dc0-121">RTM \_ notifica \_ solo \_ los \_ dests marcados</span><span class="sxs-lookup"><span data-stu-id="26dc0-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="26dc0-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="26dc0-122">0x00010000</span></span> | <span data-ttu-id="26dc0-123">Notifica al cliente los cambios en los destinos que el cliente ha marcado.</span><span class="sxs-lookup"><span data-stu-id="26dc0-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="26dc0-124">Si no se especifica esta marca, se envían los mensajes de notificación de cambios para todos los destinos.</span><span class="sxs-lookup"><span data-stu-id="26dc0-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




