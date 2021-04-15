---
title: Métodos (IManipulationProcessor)
description: Esta sección contiene los métodos de la interfaz IManipulationProcessor.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows Touch, interfaz IManipulationProcessor
- Windows Touch, métodos de interfaz
- manipulaciones, interfaz IManipulationProcessor
- Interfaz IManipulationProcessor, métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421828"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="acada-107">Métodos (IManipulationProcessor)</span><span class="sxs-lookup"><span data-stu-id="acada-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="acada-108">Esta sección contiene los métodos de la interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="acada-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="acada-109">La interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) expone los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="acada-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="acada-110">Método</span><span class="sxs-lookup"><span data-stu-id="acada-110">Method</span></span>                                                                      | <span data-ttu-id="acada-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="acada-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acada-112">**CompleteManipulation**</span><span class="sxs-lookup"><span data-stu-id="acada-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="acada-113">Se llama a este método cuando el desarrollador decide finalizar la manipulación.</span><span class="sxs-lookup"><span data-stu-id="acada-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="acada-114">**GetAngularVelocity**</span><span class="sxs-lookup"><span data-stu-id="acada-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="acada-115">Calcula la velocidad de rotación a la que se mueve el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="acada-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="acada-116">**GetExpansionVelocity**</span><span class="sxs-lookup"><span data-stu-id="acada-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="acada-117">Calcula la velocidad a la que se expande el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="acada-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="acada-118">**GetVelocityX**</span><span class="sxs-lookup"><span data-stu-id="acada-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="acada-119">Calcula y devuelve la velocidad horizontal del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="acada-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="acada-120">**GetVelocityY**</span><span class="sxs-lookup"><span data-stu-id="acada-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="acada-121">Calcula y devuelve la velocidad vertical.</span><span class="sxs-lookup"><span data-stu-id="acada-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="acada-122">**ProcessDown**</span><span class="sxs-lookup"><span data-stu-id="acada-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="acada-123">Inserta datos en el procesador de manipulación asociado a un destino.</span><span class="sxs-lookup"><span data-stu-id="acada-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="acada-124">**ProcessMove**</span><span class="sxs-lookup"><span data-stu-id="acada-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="acada-125">Inserta datos en el procesador de manipulación asociado a un destino.</span><span class="sxs-lookup"><span data-stu-id="acada-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="acada-126">**ProcessUp**</span><span class="sxs-lookup"><span data-stu-id="acada-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="acada-127">Inserta datos en el procesador de manipulación asociado a un destino.</span><span class="sxs-lookup"><span data-stu-id="acada-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="acada-128">**ProcessDownWithTime**</span><span class="sxs-lookup"><span data-stu-id="acada-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="acada-129">Inserta datos, incluida una marca de tiempo en el procesador de manipulación asociado a un destino.</span><span class="sxs-lookup"><span data-stu-id="acada-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="acada-130">**ProcessMoveWithTime**</span><span class="sxs-lookup"><span data-stu-id="acada-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="acada-131">Inserta datos, incluida una marca de tiempo en el procesador de manipulación asociado a un destino.</span><span class="sxs-lookup"><span data-stu-id="acada-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="acada-132">**ProcessUpWithTime**</span><span class="sxs-lookup"><span data-stu-id="acada-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="acada-133">Inserta datos, incluida una marca de tiempo en el procesador de manipulación asociado a un destino.</span><span class="sxs-lookup"><span data-stu-id="acada-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="acada-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acada-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acada-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="acada-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




