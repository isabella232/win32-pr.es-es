---
description: La acción CostInitialize inicia el proceso de costo de la instalación.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Acción CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667675"
---
# <a name="costinitialize-action"></a><span data-ttu-id="fc47c-103">Acción CostInitialize</span><span class="sxs-lookup"><span data-stu-id="fc47c-103">CostInitialize Action</span></span>

<span data-ttu-id="fc47c-104">La acción CostInitialize inicia el proceso de [*costo*](c-gly.md) de la instalación.</span><span class="sxs-lookup"><span data-stu-id="fc47c-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fc47c-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="fc47c-105">Sequence Restrictions</span></span>

<span data-ttu-id="fc47c-106">Cualquier acción estándar o [personalizada](custom-actions.md) que afecte a los costos se debe secuenciar antes de la acción CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="fc47c-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="fc47c-107">Llame a la acción [FileCost](filecost-action.md) inmediatamente después de la acción CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="fc47c-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="fc47c-108">Después, llame a la acción [CostFinalize](costfinalize-action.md) que sigue a la acción de acción CostInitialize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc47c-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fc47c-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="fc47c-109">ActionData Messages</span></span>

<span data-ttu-id="fc47c-110">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="fc47c-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc47c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc47c-111">Remarks</span></span>

<span data-ttu-id="fc47c-112">La acción CostInitialize carga la tabla de componentes y la tabla de [características](feature-table.md) en la memoria.</span><span class="sxs-lookup"><span data-stu-id="fc47c-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="fc47c-113">Para obtener más información sobre el proceso de [*costo*](c-gly.md) en el instalador, consulte [costo de archivos](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="fc47c-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc47c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc47c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc47c-115">Costo de archivos</span><span class="sxs-lookup"><span data-stu-id="fc47c-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



