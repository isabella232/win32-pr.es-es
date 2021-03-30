---
title: Método ShowDefaultCharacterProperties
description: Método ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775450"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="fa83f-103">Método ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="fa83f-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="fa83f-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa83f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fa83f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="fa83f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fa83f-106">Muestra las propiedades del carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fa83f-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="fa83f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="fa83f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fa83f-108">\*agente \* \* *. ShowDefaultCharacterProperties* \*  \[ *X* , *y*\]</span><span class="sxs-lookup"><span data-stu-id="fa83f-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="fa83f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fa83f-109">Part</span></span> | <span data-ttu-id="fa83f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa83f-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa83f-111">*X*</span><span class="sxs-lookup"><span data-stu-id="fa83f-111">*X*</span></span>  | <span data-ttu-id="fa83f-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fa83f-112">Optional.</span></span> <span data-ttu-id="fa83f-113">Valor entero corto que indica la coordenada de pantalla horizontal (*X* ) para mostrar la ventana.</span><span class="sxs-lookup"><span data-stu-id="fa83f-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="fa83f-114">Esta coordenada debe especificarse en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fa83f-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="fa83f-115">*S*</span><span class="sxs-lookup"><span data-stu-id="fa83f-115">*Y*</span></span>  | <span data-ttu-id="fa83f-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fa83f-116">Optional.</span></span> <span data-ttu-id="fa83f-117">Valor entero corto que indica la coordenada de pantalla vertical (*Y*) para mostrar la ventana.</span><span class="sxs-lookup"><span data-stu-id="fa83f-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="fa83f-118">Esta coordenada debe especificarse en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fa83f-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa83f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa83f-119">Remarks</span></span>

<span data-ttu-id="fa83f-120">Al llamar a este método se muestra la ventana Propiedades de carácter predeterminado (no la hoja de propiedades agente de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="fa83f-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="fa83f-121">Si no especifica las coordenadas X e y, la ventana aparecerá en la última ubicación en la que se mostró.</span><span class="sxs-lookup"><span data-stu-id="fa83f-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa83f-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa83f-122">See Also</span></span>

[<span data-ttu-id="fa83f-123">**Evento DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="fa83f-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




