---
description: La acción CCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Acción CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652596"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="3735a-103">Acción CCPSearch</span><span class="sxs-lookup"><span data-stu-id="3735a-103">CCPSearch Action</span></span>

<span data-ttu-id="3735a-104">La acción CCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.</span><span class="sxs-lookup"><span data-stu-id="3735a-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3735a-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="3735a-105">Sequence Restrictions</span></span>

<span data-ttu-id="3735a-106">La acción CCPSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="3735a-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="3735a-107">El instalador impide que la acción CCPSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ejecutó en la secuencia InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="3735a-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="3735a-108">La acción CCPSearch debe ser anterior a la acción [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3735a-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3735a-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="3735a-109">ActionData Messages</span></span>

<span data-ttu-id="3735a-110">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="3735a-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3735a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3735a-111">Remarks</span></span>

<span data-ttu-id="3735a-112">La acción CCPSearch busca las firmas de archivo enumeradas en la tabla CCPSearch del sistema con las tablas siguientes en orden: Signature, CompLocator, RegLocator, IniLocator y DrLocator.</span><span class="sxs-lookup"><span data-stu-id="3735a-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="3735a-113">Si se determina que existe alguna firma, la propiedad de **\_ éxito de CCP** se establece en 1 y la acción CCPSearch finaliza.</span><span class="sxs-lookup"><span data-stu-id="3735a-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="3735a-114">La ausencia de la firma de la tabla Signature denota un directorio.</span><span class="sxs-lookup"><span data-stu-id="3735a-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3735a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3735a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3735a-116">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="3735a-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="3735a-117">Signature</span><span class="sxs-lookup"><span data-stu-id="3735a-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="3735a-118">CompLocator</span><span class="sxs-lookup"><span data-stu-id="3735a-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="3735a-119">RegLocator</span><span class="sxs-lookup"><span data-stu-id="3735a-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="3735a-120">IniLocator</span><span class="sxs-lookup"><span data-stu-id="3735a-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="3735a-121">DrLocator</span><span class="sxs-lookup"><span data-stu-id="3735a-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



