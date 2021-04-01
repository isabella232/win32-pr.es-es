---
description: Parámetros multimedia
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parámetros multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914090"
---
# <a name="media-parameters"></a><span data-ttu-id="e0727-103">Parámetros multimedia</span><span class="sxs-lookup"><span data-stu-id="e0727-103">Media Parameters</span></span>

<span data-ttu-id="e0727-104">Los parámetros multimedia permiten a una aplicación configurar las propiedades de un objeto para que cambien a lo largo del tiempo de forma matemática.</span><span class="sxs-lookup"><span data-stu-id="e0727-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="e0727-105">Por ejemplo, supongamos que un ingeniero de sonido está mezclando una cinta maestra digital y desea aplicar un ligero retraso a una sección de voz, para rellenar el sonido.</span><span class="sxs-lookup"><span data-stu-id="e0727-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="e0727-106">El efecto será discordante si el retraso se corta de repente.</span><span class="sxs-lookup"><span data-stu-id="e0727-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="e0727-107">En su lugar, el efecto debe comenzar el 100 por ciento seco (sin retraso) y la mezcla húmeda/seco debe aumentar gradualmente hasta que alcance el nivel deseado.</span><span class="sxs-lookup"><span data-stu-id="e0727-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="e0727-108">Además, esta transición debe seguir una curva suave o una progresión lineal.</span><span class="sxs-lookup"><span data-stu-id="e0727-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="e0727-109">Para admitir este escenario, un DMO puede exponer las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="e0727-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="e0727-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contiene métodos para detectar información sobre las propiedades admitidas.</span><span class="sxs-lookup"><span data-stu-id="e0727-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="e0727-111">Normalmente, el cliente llamará a estos métodos antes de comenzar a transmitir datos.</span><span class="sxs-lookup"><span data-stu-id="e0727-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="e0727-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contiene métodos para establecer las curvas que seguirá un parámetro durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="e0727-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="e0727-113">Estas interfaces se han diseñado principalmente para DMOs, pero cualquier objeto puede admitirlos.</span><span class="sxs-lookup"><span data-stu-id="e0727-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="e0727-114">En esta sección, el término *parámetro* hace referencia a cualquier propiedad que admita estas dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="e0727-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="e0727-115">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="e0727-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e0727-116">Curvas de parámetro</span><span class="sxs-lookup"><span data-stu-id="e0727-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="e0727-117">Información de parámetros</span><span class="sxs-lookup"><span data-stu-id="e0727-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="e0727-118">Segmentos de sobre</span><span class="sxs-lookup"><span data-stu-id="e0727-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="e0727-119">Calcular valores de parámetros</span><span class="sxs-lookup"><span data-stu-id="e0727-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="e0727-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0727-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0727-121">Objetos multimedia de DirectX</span><span class="sxs-lookup"><span data-stu-id="e0727-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



