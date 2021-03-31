---
title: Destinations
description: Un destino de la tabla de enrutamiento es una entrada de red representada por una dirección de red y una máscara de red.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903541"
---
# <a name="destinations"></a><span data-ttu-id="fae38-103">Destinations</span><span class="sxs-lookup"><span data-stu-id="fae38-103">Destinations</span></span>

<span data-ttu-id="fae38-104">Un destino de la tabla de enrutamiento es una entrada de red representada por una dirección de red y una máscara de red.</span><span class="sxs-lookup"><span data-stu-id="fae38-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="fae38-105">Una entrada de destino en la tabla de enrutamiento incluye:</span><span class="sxs-lookup"><span data-stu-id="fae38-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="fae38-106">La dirección, expresada como una dirección de red y una máscara de red.</span><span class="sxs-lookup"><span data-stu-id="fae38-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="fae38-107">Una lista de rutas al destino.</span><span class="sxs-lookup"><span data-stu-id="fae38-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="fae38-108">Una lista de ranuras de puntero opacas.</span><span class="sxs-lookup"><span data-stu-id="fae38-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="fae38-109">Vistas en las que este destino es válido.</span><span class="sxs-lookup"><span data-stu-id="fae38-109">The views in which this destination is valid.</span></span> <span data-ttu-id="fae38-110">El destino contiene una estructura para cada vista que contiene la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="fae38-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="fae38-111">Identificador de la vista.</span><span class="sxs-lookup"><span data-stu-id="fae38-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="fae38-112">Puntero a la mejor ruta al destino en esta vista.</span><span class="sxs-lookup"><span data-stu-id="fae38-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="fae38-113">Propietario de la mejor ruta de esta vista.</span><span class="sxs-lookup"><span data-stu-id="fae38-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="fae38-114">Marcas asociadas a la mejor ruta en esta vista.</span><span class="sxs-lookup"><span data-stu-id="fae38-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="fae38-115">Identificador de las rutas que están en estado de suspensión en esta vista.</span><span class="sxs-lookup"><span data-stu-id="fae38-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 




