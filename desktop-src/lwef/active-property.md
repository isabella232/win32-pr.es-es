---
title: Active (propiedad)
description: Active (propiedad)
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268769"
---
# <a name="active-property"></a><span data-ttu-id="2ac88-103">Active (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2ac88-103">Active Property</span></span>

<span data-ttu-id="2ac88-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ac88-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2ac88-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="2ac88-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2ac88-106">Devuelve si la aplicación es el cliente activo del carácter y si el carácter es superior.</span><span class="sxs-lookup"><span data-stu-id="2ac88-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="2ac88-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="2ac88-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2ac88-108">\*agente. ***Caracteres \* \* \* \* ("*** CharacterID \* \* *").* \*  \[  =  *Estado* activo\]</span><span class="sxs-lookup"><span data-stu-id="2ac88-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="2ac88-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2ac88-109">Part</span></span>    | <span data-ttu-id="2ac88-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ac88-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac88-111">*state*</span><span class="sxs-lookup"><span data-stu-id="2ac88-111">*state*</span></span> | <span data-ttu-id="2ac88-112">Expresión de tipo entero que especifica el estado de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="2ac88-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="2ac88-113">0 no es el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="2ac88-113">0 Not the active client.</span></span><br/> <span data-ttu-id="2ac88-114">1 el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="2ac88-114">1 The active client.</span></span> <br/> <span data-ttu-id="2ac88-115">2 el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="2ac88-115">2 The input-active client.</span></span> <span data-ttu-id="2ac88-116">(El carácter superior).</span><span class="sxs-lookup"><span data-stu-id="2ac88-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ac88-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ac88-117">Remarks</span></span>

<span data-ttu-id="2ac88-118">Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos [**click**](click-event.md) o [DragStart](dragstart-event.md) de control de Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="2ac88-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="2ac88-119">Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe eventos de comando.</span><span class="sxs-lookup"><span data-stu-id="2ac88-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="2ac88-120">Puede usar el método [**Activate**](activate-method.md)para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (que también hace que el carácter sea más alto).</span><span class="sxs-lookup"><span data-stu-id="2ac88-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="2ac88-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2ac88-121">See Also</span></span>

[<span data-ttu-id="2ac88-122">Activar \* \* método \* \*</span><span class="sxs-lookup"><span data-stu-id="2ac88-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





