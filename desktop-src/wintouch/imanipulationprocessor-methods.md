---
title: Métodos (IInertiaProcessor)
description: Esta sección contiene los métodos de la interfaz IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, interfaz IInertiaProcessor
- Windows Touch, métodos de interfaz
- inercia, interfaz IInertiaProcessor
- Interfaz IInertiaProcessor, métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714529"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="bbda9-107">Métodos (IInertiaProcessor)</span><span class="sxs-lookup"><span data-stu-id="bbda9-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="bbda9-108">Esta sección contiene los métodos de la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="bbda9-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="bbda9-109">Método</span><span class="sxs-lookup"><span data-stu-id="bbda9-109">Method</span></span>                                                 | <span data-ttu-id="bbda9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbda9-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbda9-111">**Reset**</span><span class="sxs-lookup"><span data-stu-id="bbda9-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="bbda9-112">Inicializa el procesador con la marca de tiempo inicial y reinicia la inercia.</span><span class="sxs-lookup"><span data-stu-id="bbda9-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="bbda9-113">**Proceso**</span><span class="sxs-lookup"><span data-stu-id="bbda9-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="bbda9-114">Realiza cálculos para la marca de tiempo actual y puede generar el evento **Delta** o **completed** dependiendo de si la extrapolación se ha completado o no.</span><span class="sxs-lookup"><span data-stu-id="bbda9-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="bbda9-115">Si la extrapolación ha finalizado en el paso anterior, el método es no operativo.</span><span class="sxs-lookup"><span data-stu-id="bbda9-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="bbda9-116">**ProcessTime**</span><span class="sxs-lookup"><span data-stu-id="bbda9-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="bbda9-117">Realiza cálculos para el paso dado y puede generar el evento **Delta** o **completed** dependiendo de si la extrapolación se ha completado o no.</span><span class="sxs-lookup"><span data-stu-id="bbda9-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="bbda9-118">**Completo**</span><span class="sxs-lookup"><span data-stu-id="bbda9-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="bbda9-119">Finaliza la manipulación actual y detiene la inercia en el procesador de inercia.</span><span class="sxs-lookup"><span data-stu-id="bbda9-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="bbda9-120">**CompleteTime**</span><span class="sxs-lookup"><span data-stu-id="bbda9-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="bbda9-121">Finaliza la manipulación actual en el paso dado, detiene la inercia en el procesador de inercia y genera el evento ManipulationCompleted.</span><span class="sxs-lookup"><span data-stu-id="bbda9-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="bbda9-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bbda9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbda9-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="bbda9-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




