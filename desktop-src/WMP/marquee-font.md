---
title: Fuente de marquesina
description: Fuente de marquesina
ms.assetid: 037dce92-761a-4249-aca4-7d995cb15e7f
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b912fdaa91c84b4b6ec38fcd6716f7f4b3102c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704811"
---
# <a name="marquee-font"></a><span data-ttu-id="5f4d2-107">Fuente de marquesina</span><span class="sxs-lookup"><span data-stu-id="5f4d2-107">Marquee Font</span></span>

<span data-ttu-id="5f4d2-108">Debe definir la fuente usada por el cuadro de presentación de la marquesina que desee usar.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-108">You must define the font used by the marquee display box you wish to use.</span></span> <span data-ttu-id="5f4d2-109">La fuente se define mediante tres valores, separados por comas, que representan la superficie, el tamaño y el peso de la fuente.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-109">The font is defined by three values, separated by commas, representing the face, size, and weight of the font.</span></span>

<span data-ttu-id="5f4d2-110">**Valores de tipo de letra**</span><span class="sxs-lookup"><span data-stu-id="5f4d2-110">**Typeface Values**</span></span>

<span data-ttu-id="5f4d2-111">Se puede usar cualquier nombre de tipo de letra si es probable que esté instalado en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-111">Any typeface name can be used if it is likely to be installed on the user's machine.</span></span> <span data-ttu-id="5f4d2-112">Si no se encuentra un tipo de letra en el equipo, el sistema operativo seleccionará una alternativa.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-112">If a typeface is not found on the machine, an alternate will be selected by the operating system.</span></span> <span data-ttu-id="5f4d2-113">En la tabla siguiente se muestran los tipos de letra que suelen encontrarse en dispositivos basados en Windows Mobile 2003.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-113">The following table shows typefaces that are usually found on Windows Mobile 2003-based devices.</span></span>



| <span data-ttu-id="5f4d2-114">Tipo de letra</span><span class="sxs-lookup"><span data-stu-id="5f4d2-114">Typeface</span></span>       | <span data-ttu-id="5f4d2-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f4d2-115">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="5f4d2-116">Tahoma</span><span class="sxs-lookup"><span data-stu-id="5f4d2-116">Tahoma</span></span>         | <span data-ttu-id="5f4d2-117">Un tipo de letra sans-serif.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-117">A sans-serif typeface.</span></span>   |
| <span data-ttu-id="5f4d2-118">Lucida Console</span><span class="sxs-lookup"><span data-stu-id="5f4d2-118">Lucida Console</span></span> | <span data-ttu-id="5f4d2-119">Un tipo de letra de serif cuadrado.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-119">A square-serif typeface.</span></span> |



 

<span data-ttu-id="5f4d2-120">**Valores de tamaño**</span><span class="sxs-lookup"><span data-stu-id="5f4d2-120">**Size Values**</span></span>

<span data-ttu-id="5f4d2-121">Es el tamaño del tipo de letra en puntos.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-121">This is the size of the typeface in points.</span></span> <span data-ttu-id="5f4d2-122">Cualquier valor entero positivo es válido, aunque se recomiendan los números entre 10 y 18.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-122">Any positive integer value is valid, though numbers between 10 and 18 are recommended.</span></span> <span data-ttu-id="5f4d2-123">Los tamaños menores que 10 pueden ser difíciles de leer y los tamaños superiores a 18 no proporcionan suficiente espacio para mostrar más de unas cuantas letras a la vez.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-123">Sizes smaller than 10 may be difficult to read, and sizes above 18 may not give you enough space to display more than a few letters at a time.</span></span>

<span data-ttu-id="5f4d2-124">**Valores de peso**</span><span class="sxs-lookup"><span data-stu-id="5f4d2-124">**Weight Values**</span></span>

<span data-ttu-id="5f4d2-125">Los únicos valores permitidos se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f4d2-125">The only values allowed are shown in the following table.</span></span>



| <span data-ttu-id="5f4d2-126">Value</span><span class="sxs-lookup"><span data-stu-id="5f4d2-126">Value</span></span> | <span data-ttu-id="5f4d2-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f4d2-127">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5f4d2-128">B</span><span class="sxs-lookup"><span data-stu-id="5f4d2-128">B</span></span>     | <span data-ttu-id="5f4d2-129">Bold</span><span class="sxs-lookup"><span data-stu-id="5f4d2-129">Bold</span></span>        |
| <span data-ttu-id="5f4d2-130">N</span><span class="sxs-lookup"><span data-stu-id="5f4d2-130">N</span></span>     | <span data-ttu-id="5f4d2-131">Normal</span><span class="sxs-lookup"><span data-stu-id="5f4d2-131">Normal</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="5f4d2-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f4d2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f4d2-133">**Marquesina**</span><span class="sxs-lookup"><span data-stu-id="5f4d2-133">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




