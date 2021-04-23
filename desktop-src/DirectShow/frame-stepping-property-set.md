---
description: Conjunto de propiedades paso a paso de fotogramas
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propiedades paso a paso de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908453"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="9a6d6-103">Conjunto de propiedades paso a paso de fotogramas</span><span class="sxs-lookup"><span data-stu-id="9a6d6-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="9a6d6-104">Los descodificadores que implementan búsquedas precisas de fotogramas en Microsoft DirectShow deben implementar el conjunto de propiedades FrameStep de AM KSPROPSETID, que se usa junto con la \_ \_ interfaz [**IVideoFrameStep.**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)</span><span class="sxs-lookup"><span data-stu-id="9a6d6-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



| <span data-ttu-id="9a6d6-105">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="9a6d6-105">Label</span></span> | <span data-ttu-id="9a6d6-106">Value</span><span class="sxs-lookup"><span data-stu-id="9a6d6-106">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="9a6d6-107">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="9a6d6-107">Property Set GUID</span></span> | <span data-ttu-id="9a6d6-108">AM \_ KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="9a6d6-108">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="9a6d6-109">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="9a6d6-109">Property ID</span></span>                              | <span data-ttu-id="9a6d6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a6d6-110">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6d6-111">PASO \_ \_ FRAMESTEP DE LA \_ PROPIEDAD AM</span><span class="sxs-lookup"><span data-stu-id="9a6d6-111">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="9a6d6-112">Indica al descodificador que inicie una operación de paso y pasa una estructura [**\_ \_ FRAMESTEP de AM PROPERTY**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica el número de pasos.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-112">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="9a6d6-113">AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL</span><span class="sxs-lookup"><span data-stu-id="9a6d6-113">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="9a6d6-114">Indica al descodificador que cancele la operación de paso actual.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-114">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="9a6d6-115">No hay datos de instancia asociados a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-115">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="9a6d6-116">AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="9a6d6-116">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="9a6d6-117">El descodificador devuelve S OK en esta instrucción para indicar que puede realizar la ejecución paso a paso del marco; en caso \_ contrario, S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-117">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="9a6d6-118">Cuando se establece esta propiedad, no se pasan datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-118">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="9a6d6-119">AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="9a6d6-119">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="9a6d6-120">El descodificador devuelve S OK en esta instrucción para indicar que puede ir varios fotogramas a la vez; en caso \_ contrario, S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-120">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="9a6d6-121">Cuando se establece esta propiedad, no se pasan datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-121">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9a6d6-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a6d6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a6d6-123">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="9a6d6-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



