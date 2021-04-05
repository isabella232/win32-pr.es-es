---
title: Evento de tamaño
description: Evento de tamaño
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903393"
---
# <a name="size-event"></a><span data-ttu-id="12e08-103">Evento de tamaño</span><span class="sxs-lookup"><span data-stu-id="12e08-103">Size Event</span></span>

<span data-ttu-id="12e08-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12e08-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="12e08-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="12e08-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="12e08-106">Se produce cuando cambia el tamaño de un carácter.</span><span class="sxs-lookup"><span data-stu-id="12e08-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="12e08-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="12e08-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="12e08-108">Tamaño de **Sub** *Agent* \_ **(ByVal** *CharacterID*, **ByVal** *width*, **ByVal** *height*)</span><span class="sxs-lookup"><span data-stu-id="12e08-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="12e08-109">Parte</span><span class="sxs-lookup"><span data-stu-id="12e08-109">Part</span></span>          | <span data-ttu-id="12e08-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="12e08-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="12e08-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="12e08-111">*CharacterID*</span></span> | <span data-ttu-id="12e08-112">Devuelve el identificador del carácter que se ha despasado.</span><span class="sxs-lookup"><span data-stu-id="12e08-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="12e08-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="12e08-113">*Width*</span></span>       | <span data-ttu-id="12e08-114">Devuelve el nuevo ancho (en píxeles) del marco de caracteres como un entero.</span><span class="sxs-lookup"><span data-stu-id="12e08-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="12e08-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="12e08-115">*Height*</span></span>      | <span data-ttu-id="12e08-116">Devuelve el nuevo alto (en píxeles) del marco de caracteres como un entero.</span><span class="sxs-lookup"><span data-stu-id="12e08-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="12e08-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12e08-117">Remarks</span></span>

<span data-ttu-id="12e08-118">Este evento se produce cuando una aplicación cambia el tamaño de un carácter.</span><span class="sxs-lookup"><span data-stu-id="12e08-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="12e08-119">Este evento solo se envía a los clientes del carácter (aplicaciones que han cargado el carácter).</span><span class="sxs-lookup"><span data-stu-id="12e08-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="12e08-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12e08-120">See Also</span></span>

[<span data-ttu-id="12e08-121">**Evento de movimiento**</span><span class="sxs-lookup"><span data-stu-id="12e08-121">**Move event**</span></span>](move-event.md)


 

 




