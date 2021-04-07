---
title: Mostrar evento
description: Mostrar evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903287"
---
# <a name="show-event"></a><span data-ttu-id="5df30-103">Mostrar evento</span><span class="sxs-lookup"><span data-stu-id="5df30-103">Show Event</span></span>

<span data-ttu-id="5df30-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5df30-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5df30-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="5df30-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5df30-106">Se produce cuando se muestra un carácter.</span><span class="sxs-lookup"><span data-stu-id="5df30-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5df30-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="5df30-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5df30-108">**Sub** *Agent \* \* \* \_ Show (ByVal* \*  *CharacterID*, **ByVal** *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="5df30-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="5df30-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5df30-109">Part</span></span>          | <span data-ttu-id="5df30-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5df30-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df30-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5df30-111">*CharacterID*</span></span> | <span data-ttu-id="5df30-112">Devuelve el identificador del carácter que se muestra como una cadena.</span><span class="sxs-lookup"><span data-stu-id="5df30-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="5df30-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="5df30-113">*Cause*</span></span>       | <span data-ttu-id="5df30-114">Devuelve un valor que indica la causa del carácter que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="5df30-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="5df30-115">2 el usuario mostró el carácter (mediante el comando de menú o de voz).</span><span class="sxs-lookup"><span data-stu-id="5df30-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="5df30-116">4 la aplicación cliente mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="5df30-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="5df30-117">6 otra aplicación cliente mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="5df30-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5df30-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5df30-118">Remarks</span></span>

<span data-ttu-id="5df30-119">El servidor envía este evento a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="5df30-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="5df30-120">Para consultar el estado actual del carácter, utilice la propiedad [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="5df30-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="5df30-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5df30-121">See Also</span></span>

<span data-ttu-id="5df30-122">[**Ocultar evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="5df30-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





