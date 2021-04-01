---
description: Transición de clave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transición de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906445"
---
# <a name="key-transition"></a><span data-ttu-id="249a8-103">Transición de clave</span><span class="sxs-lookup"><span data-stu-id="249a8-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="249a8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="249a8-104">\[Deprecated.</span></span> <span data-ttu-id="249a8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="249a8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="249a8-106">La transición de clave realiza la creación de claves según el valor RGB, el valor alfa, el matiz o la luminancia.</span><span class="sxs-lookup"><span data-stu-id="249a8-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="249a8-107">La siguiente imagen muestra la transición de la clave:</span><span class="sxs-lookup"><span data-stu-id="249a8-107">The following image shows the key transition:</span></span>

![transición de clave](images/trans-key.png)

<span data-ttu-id="249a8-109">IDENTIFICADOR de clase (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="249a8-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="249a8-110">Nombre de la variable CLSID: CLSID \_ DxtKey</span><span class="sxs-lookup"><span data-stu-id="249a8-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="249a8-111">Nombre descriptivo: "DxtKey"</span><span class="sxs-lookup"><span data-stu-id="249a8-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="249a8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="249a8-112">Properties</span></span>



| <span data-ttu-id="249a8-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="249a8-113">Property</span></span>   | <span data-ttu-id="249a8-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="249a8-114">Type</span></span>  | <span data-ttu-id="249a8-115">Intervalo válido</span><span class="sxs-lookup"><span data-stu-id="249a8-115">Valid range</span></span>           | <span data-ttu-id="249a8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="249a8-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="249a8-117">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="249a8-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="249a8-118">Matiz</span><span class="sxs-lookup"><span data-stu-id="249a8-118">Hue</span></span>        | <span data-ttu-id="249a8-119">int</span><span class="sxs-lookup"><span data-stu-id="249a8-119">int</span></span>   | <span data-ttu-id="249a8-120">de 0 a 360</span><span class="sxs-lookup"><span data-stu-id="249a8-120">0–360</span></span>                 | <span data-ttu-id="249a8-121">Valor de matiz en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="249a8-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="249a8-122">Matiz</span><span class="sxs-lookup"><span data-stu-id="249a8-122">Hue</span></span>                            |
| <span data-ttu-id="249a8-123">Invertir</span><span class="sxs-lookup"><span data-stu-id="249a8-123">Invert</span></span>     | <span data-ttu-id="249a8-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="249a8-124">BOOL</span></span>  | <span data-ttu-id="249a8-125">**False** o **true**</span><span class="sxs-lookup"><span data-stu-id="249a8-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="249a8-126">Valor booleano que indica si se va a invertir la operación predeterminada de la clave.</span><span class="sxs-lookup"><span data-stu-id="249a8-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="249a8-127">Si **es false**, los píxeles de la imagen superpuestas se convierten en transparentes de la manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="249a8-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="249a8-128">Si **es true**, la operación invierte.</span><span class="sxs-lookup"><span data-stu-id="249a8-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="249a8-129">Croma, matiz, luminancia, Nonred</span><span class="sxs-lookup"><span data-stu-id="249a8-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="249a8-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="249a8-130">KeyType</span></span>    | <span data-ttu-id="249a8-131">int</span><span class="sxs-lookup"><span data-stu-id="249a8-131">int</span></span>   | <span data-ttu-id="249a8-132">Ver comentarios</span><span class="sxs-lookup"><span data-stu-id="249a8-132">See Remarks</span></span>           | <span data-ttu-id="249a8-133">Especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="249a8-133">Specifies the type of key.</span></span> <span data-ttu-id="249a8-134">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="249a8-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="249a8-135">All</span><span class="sxs-lookup"><span data-stu-id="249a8-135">All</span></span>                            |
| <span data-ttu-id="249a8-136">Luminance</span><span class="sxs-lookup"><span data-stu-id="249a8-136">Luminance</span></span>  | <span data-ttu-id="249a8-137">int</span><span class="sxs-lookup"><span data-stu-id="249a8-137">int</span></span>   | <span data-ttu-id="249a8-138">de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="249a8-138">0–100</span></span>                 | <span data-ttu-id="249a8-139">Valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="249a8-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="249a8-140">Luminance</span><span class="sxs-lookup"><span data-stu-id="249a8-140">Luminance</span></span>                      |
| <span data-ttu-id="249a8-141">RGB</span><span class="sxs-lookup"><span data-stu-id="249a8-141">RGB</span></span>        | <span data-ttu-id="249a8-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="249a8-142">DWORD</span></span> | <span data-ttu-id="249a8-143">0X0:0xFFFFFF</span><span class="sxs-lookup"><span data-stu-id="249a8-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="249a8-144">Color en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="249a8-144">The color on which to key.</span></span> <span data-ttu-id="249a8-145">El valor es un número hexadecimal con el formato 0x *RRGGBB*, donde *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul.</span><span class="sxs-lookup"><span data-stu-id="249a8-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="249a8-146">(Rojo puro, verde y azul son 0xFF0000, 0x00FF00 y 0x0000FF, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="249a8-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="249a8-147">Adapta</span><span class="sxs-lookup"><span data-stu-id="249a8-147">Chroma</span></span>                         |
| <span data-ttu-id="249a8-148">Similitud</span><span class="sxs-lookup"><span data-stu-id="249a8-148">Similarity</span></span> | <span data-ttu-id="249a8-149">int</span><span class="sxs-lookup"><span data-stu-id="249a8-149">int</span></span>   | <span data-ttu-id="249a8-150">de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="249a8-150">0–100</span></span>                 | <span data-ttu-id="249a8-151">El intervalo de datos de color que se vuelve transparente.</span><span class="sxs-lookup"><span data-stu-id="249a8-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="249a8-152">En los valores más altos, una mayor variedad de colores similares es transparente.</span><span class="sxs-lookup"><span data-stu-id="249a8-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="249a8-153">Croma, Nonred</span><span class="sxs-lookup"><span data-stu-id="249a8-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="249a8-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="249a8-154">Remarks</span></span>

<span data-ttu-id="249a8-155">El tipo de clave que se realiza depende del valor de la propiedad **KeyType** , que debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="249a8-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="249a8-156">Value</span><span class="sxs-lookup"><span data-stu-id="249a8-156">Value</span></span> | <span data-ttu-id="249a8-157">Enumeración</span><span class="sxs-lookup"><span data-stu-id="249a8-157">Enumeration</span></span>       | <span data-ttu-id="249a8-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="249a8-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="249a8-159">0</span><span class="sxs-lookup"><span data-stu-id="249a8-159">0</span></span>     | <span data-ttu-id="249a8-160">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="249a8-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="249a8-161">Clave de croma (clave por valor RGB).</span><span class="sxs-lookup"><span data-stu-id="249a8-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="249a8-162">1</span><span class="sxs-lookup"><span data-stu-id="249a8-162">1</span></span>     | <span data-ttu-id="249a8-163">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="249a8-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="249a8-164">Clave Nonred.</span><span class="sxs-lookup"><span data-stu-id="249a8-164">Nonred key.</span></span> <span data-ttu-id="249a8-165">(Hace que las áreas azules y verdes sean transparentes).</span><span class="sxs-lookup"><span data-stu-id="249a8-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="249a8-166">2</span><span class="sxs-lookup"><span data-stu-id="249a8-166">2</span></span>     | <span data-ttu-id="249a8-167">\_luminancia DXTKEY</span><span class="sxs-lookup"><span data-stu-id="249a8-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="249a8-168">Clave de luminancia.</span><span class="sxs-lookup"><span data-stu-id="249a8-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="249a8-169">3</span><span class="sxs-lookup"><span data-stu-id="249a8-169">3</span></span>     | <span data-ttu-id="249a8-170">\_alfa DXTKEY</span><span class="sxs-lookup"><span data-stu-id="249a8-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="249a8-171">Clave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="249a8-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="249a8-172">4</span><span class="sxs-lookup"><span data-stu-id="249a8-172">4</span></span>     | <span data-ttu-id="249a8-173">\_matiz DXTKEY</span><span class="sxs-lookup"><span data-stu-id="249a8-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="249a8-174">Clave por matiz.</span><span class="sxs-lookup"><span data-stu-id="249a8-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="249a8-175">De forma predeterminada, el tipo de clave es DXTKEY \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="249a8-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



