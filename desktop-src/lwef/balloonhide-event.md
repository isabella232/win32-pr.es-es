---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269300"
---
# <a name="balloonhide-event"></a><span data-ttu-id="e7707-103">Evento BalloonHide</span><span class="sxs-lookup"><span data-stu-id="e7707-103">BalloonHide Event</span></span>

<span data-ttu-id="e7707-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7707-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e7707-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="e7707-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e7707-106">Se produce cuando se oculta el globo de palabras de un carácter.</span><span class="sxs-lookup"><span data-stu-id="e7707-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="e7707-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="e7707-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e7707-108">**Sub** *Agent* \_ **BalloonHide** **(ByVal** \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="e7707-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="e7707-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e7707-109">Part</span></span>          | <span data-ttu-id="e7707-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7707-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="e7707-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="e7707-111">*CharacterID*</span></span> | <span data-ttu-id="e7707-112">Devuelve el identificador del carácter asociado al globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="e7707-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="e7707-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7707-113">Remarks</span></span>

<span data-ttu-id="e7707-114">El servidor envía este evento solo a los clientes del carácter (aplicaciones que han cargado el carácter) que usa el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="e7707-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="e7707-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7707-115">See Also</span></span>

[<span data-ttu-id="e7707-116">**Evento BalloonShow**</span><span class="sxs-lookup"><span data-stu-id="e7707-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




