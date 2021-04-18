---
title: Grupos de atributos
description: Grupos de atributos
ms.assetid: 9fd7dc6e-6749-4e32-b795-21b63b64c291
keywords:
- OpenGL, grupos de atributos
- Referencia de OpenGL, grupos de atributos
- referencia de OpenGL, grupos de atributos
- grupos de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d93582c8996438ad99d7bf896cf83bdf6fbf72d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676151"
---
# <a name="attribute-groups"></a><span data-ttu-id="27942-107">Grupos de atributos</span><span class="sxs-lookup"><span data-stu-id="27942-107">Attribute Groups</span></span>



| <span data-ttu-id="27942-108">Bit de máscara</span><span class="sxs-lookup"><span data-stu-id="27942-108">Mask bit</span></span>                  | <span data-ttu-id="27942-109">Grupo de atributos</span><span class="sxs-lookup"><span data-stu-id="27942-109">Attribute group</span></span> |
|---------------------------|-----------------|
| <span data-ttu-id="27942-110">\_bit de \_ búfer de acumulación de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-110">GL\_ACCUM\_BUFFER\_BIT</span></span>    | <span data-ttu-id="27942-111">búfer acumulado</span><span class="sxs-lookup"><span data-stu-id="27942-111">accum-buffer</span></span>    |
| <span data-ttu-id="27942-112">núm. \_ todos los \_ \_ bits attrib</span><span class="sxs-lookup"><span data-stu-id="27942-112">GL\_ALL\_ATTRIB\_BITS</span></span>     |                 |
| <span data-ttu-id="27942-113">\_bit de \_ búfer de color de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-113">GL\_COLOR\_BUFFER\_BIT</span></span>    | <span data-ttu-id="27942-114">búfer de color</span><span class="sxs-lookup"><span data-stu-id="27942-114">color-buffer</span></span>    |
| <span data-ttu-id="27942-115">\_bits actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-115">GL\_CURRENT\_BIT</span></span>          | <span data-ttu-id="27942-116">actuales</span><span class="sxs-lookup"><span data-stu-id="27942-116">current</span></span>         |
| <span data-ttu-id="27942-117">\_bit de \_ búfer de profundidad de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-117">GL\_DEPTH\_BUFFER\_BIT</span></span>    | <span data-ttu-id="27942-118">búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="27942-118">depth-buffer</span></span>    |
| <span data-ttu-id="27942-119">\_bit de habilitación de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-119">GL\_ENABLE\_BIT</span></span>           | <span data-ttu-id="27942-120">enable</span><span class="sxs-lookup"><span data-stu-id="27942-120">enable</span></span>          |
| <span data-ttu-id="27942-121">\_bit de evaluación de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-121">GL\_EVAL\_BIT</span></span>             | <span data-ttu-id="27942-122">eval</span><span class="sxs-lookup"><span data-stu-id="27942-122">eval</span></span>            |
| <span data-ttu-id="27942-123">\_bit de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-123">GL\_FOG\_BIT</span></span>              | <span data-ttu-id="27942-124">luz</span><span class="sxs-lookup"><span data-stu-id="27942-124">fog</span></span>             |
| <span data-ttu-id="27942-125">\_bit de sugerencia de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-125">GL\_HINT\_BIT</span></span>             | <span data-ttu-id="27942-126">sugerencia</span><span class="sxs-lookup"><span data-stu-id="27942-126">hint</span></span>            |
| <span data-ttu-id="27942-127">\_bit de iluminación de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-127">GL\_LIGHTING\_BIT</span></span>         | <span data-ttu-id="27942-128">iluminación</span><span class="sxs-lookup"><span data-stu-id="27942-128">lighting</span></span>        |
| <span data-ttu-id="27942-129">\_bit de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-129">GL\_LINE\_BIT</span></span>             | <span data-ttu-id="27942-130">line</span><span class="sxs-lookup"><span data-stu-id="27942-130">line</span></span>            |
| <span data-ttu-id="27942-131">\_bit de lista de contab. \_</span><span class="sxs-lookup"><span data-stu-id="27942-131">GL\_LIST\_BIT</span></span>             | <span data-ttu-id="27942-132">list</span><span class="sxs-lookup"><span data-stu-id="27942-132">list</span></span>            |
| <span data-ttu-id="27942-133">\_bit de \_ modo de píxel de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-133">GL\_PIXEL\_MODE\_BIT</span></span>      | <span data-ttu-id="27942-134">píxel</span><span class="sxs-lookup"><span data-stu-id="27942-134">pixel</span></span>           |
| <span data-ttu-id="27942-135">\_bit de punta de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-135">GL\_POINT\_BIT</span></span>            | <span data-ttu-id="27942-136">point</span><span class="sxs-lookup"><span data-stu-id="27942-136">point</span></span>           |
| <span data-ttu-id="27942-137">\_bit de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-137">GL\_POLYGON\_BIT</span></span>          | <span data-ttu-id="27942-138">polygon</span><span class="sxs-lookup"><span data-stu-id="27942-138">polygon</span></span>         |
| <span data-ttu-id="27942-139">\_bit de \_ punteado de los polígonos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-139">GL\_POLYGON\_STIPPLE\_BIT</span></span> | <span data-ttu-id="27942-140">Polígono-punteado</span><span class="sxs-lookup"><span data-stu-id="27942-140">polygon-stipple</span></span> |
| <span data-ttu-id="27942-141">\_bit de tijera de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-141">GL\_SCISSOR\_BIT</span></span>          | <span data-ttu-id="27942-142">tijera</span><span class="sxs-lookup"><span data-stu-id="27942-142">scissor</span></span>         |
| <span data-ttu-id="27942-143">\_bit de \_ búfer de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-143">GL\_STENCIL\_BUFFER\_BIT</span></span>  | <span data-ttu-id="27942-144">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="27942-144">stencil-buffer</span></span>  |
| <span data-ttu-id="27942-145">\_bit de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-145">GL\_TEXTURE\_BIT</span></span>          | <span data-ttu-id="27942-146">textura</span><span class="sxs-lookup"><span data-stu-id="27942-146">texture</span></span>         |
| <span data-ttu-id="27942-147">\_bit de transformación de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="27942-147">GL\_TRANSFORM\_BIT</span></span>        | <span data-ttu-id="27942-148">transform</span><span class="sxs-lookup"><span data-stu-id="27942-148">transform</span></span>       |
| <span data-ttu-id="27942-149">\_bit de ventanilla de GL \_</span><span class="sxs-lookup"><span data-stu-id="27942-149">GL\_VIEWPORT\_BIT</span></span>         | <span data-ttu-id="27942-150">ventanilla</span><span class="sxs-lookup"><span data-stu-id="27942-150">viewport</span></span>        |



 

 

 




