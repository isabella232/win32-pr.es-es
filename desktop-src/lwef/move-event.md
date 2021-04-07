---
title: Evento de movimiento
description: Evento de movimiento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903506"
---
# <a name="move-event"></a><span data-ttu-id="30379-103">Evento de movimiento</span><span class="sxs-lookup"><span data-stu-id="30379-103">Move Event</span></span>

<span data-ttu-id="30379-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30379-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="30379-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="30379-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="30379-106">Se produce cuando se mueve un carácter.</span><span class="sxs-lookup"><span data-stu-id="30379-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="30379-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="30379-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="30379-108">**Sub** *Agent* \_ **Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="30379-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="30379-109">Parte</span><span class="sxs-lookup"><span data-stu-id="30379-109">Part</span></span>          | <span data-ttu-id="30379-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="30379-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30379-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="30379-111">*CharacterID*</span></span> | <span data-ttu-id="30379-112">Devuelve el identificador del carácter que se ha despasado.</span><span class="sxs-lookup"><span data-stu-id="30379-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="30379-113">*X*</span><span class="sxs-lookup"><span data-stu-id="30379-113">*X*</span></span>           | <span data-ttu-id="30379-114">Devuelve la coordenada x (en píxeles) del borde superior de la nueva ubicación del marco de caracteres como un entero.</span><span class="sxs-lookup"><span data-stu-id="30379-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="30379-115">*S*</span><span class="sxs-lookup"><span data-stu-id="30379-115">*Y*</span></span>           | <span data-ttu-id="30379-116">Devuelve la coordenada y (en píxeles) del borde izquierdo de la nueva ubicación del marco de caracteres como un entero.</span><span class="sxs-lookup"><span data-stu-id="30379-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="30379-117">*Causa*</span><span class="sxs-lookup"><span data-stu-id="30379-117">*Cause*</span></span>       | <span data-ttu-id="30379-118">Devuelve un valor que indica lo que ha provocado el movimiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="30379-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="30379-119">1 el usuario arrastró el carácter.</span><span class="sxs-lookup"><span data-stu-id="30379-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="30379-120">2 la aplicación cliente ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="30379-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="30379-121">3 otra aplicación cliente ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="30379-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="30379-122">4 el servidor del agente ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="30379-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="30379-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30379-123">Remarks</span></span>

<span data-ttu-id="30379-124">Este evento se produce cuando el usuario o una aplicación cambian la posición del carácter.</span><span class="sxs-lookup"><span data-stu-id="30379-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="30379-125">Las coordenadas son relevantes en la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="30379-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="30379-126">Este evento solo se envía a los clientes del carácter (aplicaciones que han cargado el carácter).</span><span class="sxs-lookup"><span data-stu-id="30379-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="30379-127">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="30379-127">**See Also**</span></span>

<span data-ttu-id="30379-128">[**Propiedad MoveCause**](movecause-property.md), [ **evento size**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="30379-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 





