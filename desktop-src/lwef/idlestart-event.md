---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714175"
---
# <a name="idlestart-event"></a><span data-ttu-id="a3776-103">Evento IdleStart</span><span class="sxs-lookup"><span data-stu-id="a3776-103">IdleStart Event</span></span>

<span data-ttu-id="a3776-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3776-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a3776-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a3776-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a3776-106">Se produce cuando el servidor establece un carácter en el estado de **ralentí** .</span><span class="sxs-lookup"><span data-stu-id="a3776-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="a3776-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a3776-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a3776-108">**Sub** *Agent \* \* \* \_ IdleStart* \*  **(ByVal** \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="a3776-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="a3776-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a3776-109">Part</span></span>          | <span data-ttu-id="a3776-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3776-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="a3776-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="a3776-111">*CharacterID*</span></span> | <span data-ttu-id="a3776-112">Devuelve el identificador del carácter de ralentí como una cadena.</span><span class="sxs-lookup"><span data-stu-id="a3776-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="a3776-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3776-113">Remarks</span></span>

<span data-ttu-id="a3776-114">El servidor envía este evento a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="a3776-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="a3776-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3776-115">See Also</span></span>

[<span data-ttu-id="a3776-116">**Evento IdleComplete**</span><span class="sxs-lookup"><span data-stu-id="a3776-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




