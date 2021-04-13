---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418966"
---
# <a name="balloonshow-event"></a><span data-ttu-id="a65f9-103">Evento BalloonShow</span><span class="sxs-lookup"><span data-stu-id="a65f9-103">BalloonShow Event</span></span>

<span data-ttu-id="a65f9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a65f9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a65f9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a65f9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a65f9-106">Se produce cuando se muestra el globo de palabras de un carácter.</span><span class="sxs-lookup"><span data-stu-id="a65f9-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="a65f9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a65f9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a65f9-108">**Sub** *Agent* \_ **BalloonShow** **(ByVal** \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="a65f9-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="a65f9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a65f9-109">Part</span></span>          | <span data-ttu-id="a65f9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a65f9-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="a65f9-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="a65f9-111">*CharacterID*</span></span> | <span data-ttu-id="a65f9-112">Devuelve el identificador del carácter asociado al globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="a65f9-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="a65f9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a65f9-113">Remarks</span></span>

<span data-ttu-id="a65f9-114">El servidor envía este evento solo a los clientes del carácter (aplicaciones que han cargado el carácter) que usa el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="a65f9-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="a65f9-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a65f9-115">See Also</span></span>

[<span data-ttu-id="a65f9-116">**Evento BalloonHide**</span><span class="sxs-lookup"><span data-stu-id="a65f9-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




