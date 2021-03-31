---
description: Conjunto de propiedades de ejecución de fotogramas
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propiedades de ejecución de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806128"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="453ea-103">Conjunto de propiedades de ejecución de fotogramas</span><span class="sxs-lookup"><span data-stu-id="453ea-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="453ea-104">Los descodificadores que implementan búsquedas con precisión de fotogramas en Microsoft DirectShow deben implementar el \_ conjunto de propiedades AM KSPROPSETID \_ FrameStep, que se usa junto con la interfaz [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="453ea-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="453ea-105">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="453ea-105">Property Set GUID</span></span> | <span data-ttu-id="453ea-106">\_FrameStep KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="453ea-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="453ea-107">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="453ea-107">Property ID</span></span>                              | <span data-ttu-id="453ea-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="453ea-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="453ea-109">FRAMESTEP de la \_ propiedad AM \_ \_ paso</span><span class="sxs-lookup"><span data-stu-id="453ea-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="453ea-110">Indica al descodificador que comience una operación de paso y pasa una [**estructura \_ \_ FRAMESTEP de la propiedad AM**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica el número de pasos.</span><span class="sxs-lookup"><span data-stu-id="453ea-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="453ea-111">\_propiedad AM \_ FRAMESTEP \_ cancelar</span><span class="sxs-lookup"><span data-stu-id="453ea-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="453ea-112">Indica al descodificador que cancele la operación de paso actual.</span><span class="sxs-lookup"><span data-stu-id="453ea-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="453ea-113">No hay datos de instancia asociados a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="453ea-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="453ea-114">\_propiedad AM \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="453ea-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="453ea-115">El descodificador devuelve S \_ OK en esta instrucción para indicar que puede realizar la ejecución paso a paso de fotogramas; de \_ lo contrario, es false.</span><span class="sxs-lookup"><span data-stu-id="453ea-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="453ea-116">No se pasan datos de instancia cuando se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="453ea-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="453ea-117">\_propiedad AM \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="453ea-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="453ea-118">El descodificador devuelve S \_ OK en esta instrucción para indicar que puede recorrer varios fotogramas a la vez; de \_ lo contrario, es false.</span><span class="sxs-lookup"><span data-stu-id="453ea-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="453ea-119">No se pasan datos de instancia cuando se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="453ea-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="453ea-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="453ea-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="453ea-121">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="453ea-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



