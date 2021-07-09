---
description: Obtenga información sobre la compatibilidad con los deltas de PrintTicket. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Compatibilidad con printticket deltas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548789"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="e5ac0-105">Compatibilidad con printticket deltas</span><span class="sxs-lookup"><span data-stu-id="e5ac0-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="e5ac0-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-106">This topic is not current.</span></span> <span data-ttu-id="e5ac0-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e5ac0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e5ac0-108">La interfaz del proveedor PrintTicket tiene métodos que se pueden usar para realizar cambios incrementales en un PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="e5ac0-109">Los cambios incrementales de PrintTicket se pueden especificar en un PrintTicket parcial que se conoce como printTicket delta.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="e5ac0-110">Se crea un PrintTicket revisado combinando un valor delta de PrintTicket con un PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="e5ac0-111">Consulte el próximo documento de la interfaz del proveedor PrintTicket para obtener más información sobre los métodos que implican los deltas de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="e5ac0-112">Cuando se procesa un delta de PrintTicket, se deben realizar los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="e5ac0-113">Identifique las instancias de Feature o ParameterInit que son comunes tanto a la clase PrintTicket existente (printTicket de destino) como a la diferencia PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="e5ac0-114">Para cada característica común a la diferencia PrintTicket y PrintTicket de destino, reemplace la característica en el PrintTicket de destino por la característica correspondiente en la diferencia PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="e5ac0-115">Para cada ParameterInit común a la propiedad PrintTicket de destino y a la diferencia PrintTicket, reemplace ParameterInit en el PrintTicket de destino por el parámetro ParameterInit correspondiente en el delta de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="e5ac0-116">Copie todas las instancias de Feature y ParameterInit restantes de la diferencia PrintTicket en el PrintTicket de destino.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="e5ac0-117">Si el algoritmo de resolución de conflictos permite especificar prioridades en el propio PrintTicket, puede elegir elevar las prioridades de las instancias Feature y ParameterInit denominadas en la diferencia PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e5ac0-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="e5ac0-118">Realice la validación de PrintTicket como se describe en [Lista de comprobación de validación de PrintTicket.](printticket-validation-checklist.md)</span><span class="sxs-lookup"><span data-stu-id="e5ac0-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5ac0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5ac0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5ac0-120">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e5ac0-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



