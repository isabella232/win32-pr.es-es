---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Compatibilidad con diferencias de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707619"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="adeae-104">Compatibilidad con diferencias de PrintTicket</span><span class="sxs-lookup"><span data-stu-id="adeae-104">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="adeae-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="adeae-105">This topic is not current.</span></span> <span data-ttu-id="adeae-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="adeae-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="adeae-107">La interfaz del proveedor PrintTicket tiene métodos que se pueden usar para realizar cambios incrementales en un PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="adeae-107">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="adeae-108">Los cambios incrementales de PrintTicket se pueden especificar en un PrintTicket parcial que se conoce como una diferencia de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="adeae-108">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="adeae-109">Se crea un PrintTicket revisado mediante la combinación de una diferencia de PrintTicket con un PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="adeae-109">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="adeae-110">Vea el documento sobre la interfaz del proveedor de PrintTicket próximamente para obtener más información sobre los métodos que implican diferencias de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="adeae-110">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="adeae-111">Cuando se procesa una diferencia de PrintTicket, se deben realizar los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="adeae-111">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="adeae-112">Identifique las instancias de Feature o ParameterInit que son comunes al PrintTicket existente (el PrintTicket de destino) y la diferencia de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="adeae-112">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="adeae-113">Para cada característica común al PrintTicket de destino y al delta de PrintTicket, reemplace la característica en el PrintTicket de destino por la característica correspondiente en la diferencia de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="adeae-113">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="adeae-114">Para cada ParameterInit común al PrintTicket de destino y al delta de PrintTicket, reemplace el ParameterInit en el PrintTicket de destino por el ParameterInit correspondiente en la diferencia de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="adeae-114">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="adeae-115">Copie todas las instancias de Feature y ParameterInit restantes en la diferencia de PrintTicket en el PrintTicket de destino.</span><span class="sxs-lookup"><span data-stu-id="adeae-115">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="adeae-116">Si el algoritmo de resolución de conflictos permite que se especifiquen prioridades en el propio PrintTicket, puede optar por elevar las prioridades de la característica y las instancias de ParameterInit mencionadas en la diferencia de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="adeae-116">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="adeae-117">Realice la validación de PrintTicket como se describe en la [lista de comprobación de validación de PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="adeae-117">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adeae-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="adeae-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adeae-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="adeae-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



