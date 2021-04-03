---
title: Evento IdleComplete
description: Evento IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074983"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="5396e-103">Evento IdleComplete</span><span class="sxs-lookup"><span data-stu-id="5396e-103">IdleComplete Event</span></span>

<span data-ttu-id="5396e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5396e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5396e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="5396e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5396e-106">Se produce cuando el servidor finaliza el estado de **ralentí** de un carácter.</span><span class="sxs-lookup"><span data-stu-id="5396e-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="5396e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="5396e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5396e-108">**Sub** *Agent \* \* \* \_ IdleComplete* \*  **(ByVal** \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="5396e-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="5396e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5396e-109">Part</span></span>          | <span data-ttu-id="5396e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5396e-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="5396e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5396e-111">*CharacterID*</span></span> | <span data-ttu-id="5396e-112">Devuelve el identificador del carácter de ralentí como una cadena.</span><span class="sxs-lookup"><span data-stu-id="5396e-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5396e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5396e-113">Remarks</span></span>

<span data-ttu-id="5396e-114">El servidor envía este evento a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="5396e-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="5396e-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5396e-115">See Also</span></span>

[<span data-ttu-id="5396e-116">**Evento IdleStart**</span><span class="sxs-lookup"><span data-stu-id="5396e-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




