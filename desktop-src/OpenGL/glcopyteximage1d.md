---
title: función glCopyTexImage1D (GL. h)
description: La función glCopyTexImage1D copia píxeles de la fotogramas en una imagen de textura de una dimensión.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- glCopyTexImage1D (función) OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666039"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="cf277-104">glCopyTexImage1D función)</span><span class="sxs-lookup"><span data-stu-id="cf277-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="cf277-105">La función **glCopyTexImage1D** copia píxeles de la fotogramas en una imagen de textura de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="cf277-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf277-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf277-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="cf277-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf277-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf277-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="cf277-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-109">Destino para el que se cambiarán los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf277-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="cf277-110">Debe tener el valor de GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="cf277-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="cf277-111">*level*</span><span class="sxs-lookup"><span data-stu-id="cf277-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-112">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="cf277-112">The level-of-detail number.</span></span> <span data-ttu-id="cf277-113">El nivel 0 es la imagen base.</span><span class="sxs-lookup"><span data-stu-id="cf277-113">Level 0 is the base image.</span></span> <span data-ttu-id="cf277-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="cf277-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="cf277-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="cf277-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-116">El formato interno y la resolución de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="cf277-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="cf277-117">Este parámetro debe ser uno de los siguientes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="cf277-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="cf277-118">Constante</span><span class="sxs-lookup"><span data-stu-id="cf277-118">Constant</span></span>                 | <span data-ttu-id="cf277-119">Bits R</span><span class="sxs-lookup"><span data-stu-id="cf277-119">R Bits</span></span> | <span data-ttu-id="cf277-120">G bits</span><span class="sxs-lookup"><span data-stu-id="cf277-120">G Bits</span></span> | <span data-ttu-id="cf277-121">Bits B</span><span class="sxs-lookup"><span data-stu-id="cf277-121">B Bits</span></span> | <span data-ttu-id="cf277-122">Un bits</span><span class="sxs-lookup"><span data-stu-id="cf277-122">A Bits</span></span> | <span data-ttu-id="cf277-123">Bits L</span><span class="sxs-lookup"><span data-stu-id="cf277-123">L Bits</span></span> | <span data-ttu-id="cf277-124">I bits</span><span class="sxs-lookup"><span data-stu-id="cf277-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="cf277-125">libro \_ de contabilidad</span><span class="sxs-lookup"><span data-stu-id="cf277-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="cf277-126">GL \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="cf277-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="cf277-127">4</span><span class="sxs-lookup"><span data-stu-id="cf277-127">4</span></span>      |        |        |
| <span data-ttu-id="cf277-128">GL \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="cf277-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="cf277-129">8</span><span class="sxs-lookup"><span data-stu-id="cf277-129">8</span></span>      |        |        |
| <span data-ttu-id="cf277-130">GL \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="cf277-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="cf277-131">12</span><span class="sxs-lookup"><span data-stu-id="cf277-131">12</span></span>     |        |        |
| <span data-ttu-id="cf277-132">GL \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="cf277-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="cf277-133">16</span><span class="sxs-lookup"><span data-stu-id="cf277-133">16</span></span>     |        |        |
| <span data-ttu-id="cf277-134">luminancia del libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="cf277-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="cf277-135">GL \_ LUMINANCE4</span><span class="sxs-lookup"><span data-stu-id="cf277-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="cf277-136">4</span><span class="sxs-lookup"><span data-stu-id="cf277-136">4</span></span>      |        |
| <span data-ttu-id="cf277-137">GL \_ LUMINANCE8</span><span class="sxs-lookup"><span data-stu-id="cf277-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="cf277-138">8</span><span class="sxs-lookup"><span data-stu-id="cf277-138">8</span></span>      |        |
| <span data-ttu-id="cf277-139">GL \_ LUMINANCE12</span><span class="sxs-lookup"><span data-stu-id="cf277-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="cf277-140">12</span><span class="sxs-lookup"><span data-stu-id="cf277-140">12</span></span>     |        |
| <span data-ttu-id="cf277-141">GL \_ LUMINANCE16</span><span class="sxs-lookup"><span data-stu-id="cf277-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="cf277-142">16</span><span class="sxs-lookup"><span data-stu-id="cf277-142">16</span></span>     |        |
| <span data-ttu-id="cf277-143">alfa de luminancia de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="cf277-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="cf277-144">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="cf277-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="cf277-145">4</span><span class="sxs-lookup"><span data-stu-id="cf277-145">4</span></span>      | <span data-ttu-id="cf277-146">4</span><span class="sxs-lookup"><span data-stu-id="cf277-146">4</span></span>      |        |
| <span data-ttu-id="cf277-147">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="cf277-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="cf277-148">2</span><span class="sxs-lookup"><span data-stu-id="cf277-148">2</span></span>      | <span data-ttu-id="cf277-149">6</span><span class="sxs-lookup"><span data-stu-id="cf277-149">6</span></span>      |        |
| <span data-ttu-id="cf277-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="cf277-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="cf277-151">8</span><span class="sxs-lookup"><span data-stu-id="cf277-151">8</span></span>      | <span data-ttu-id="cf277-152">8</span><span class="sxs-lookup"><span data-stu-id="cf277-152">8</span></span>      |        |
| <span data-ttu-id="cf277-153">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="cf277-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="cf277-154">4</span><span class="sxs-lookup"><span data-stu-id="cf277-154">4</span></span>      | <span data-ttu-id="cf277-155">12</span><span class="sxs-lookup"><span data-stu-id="cf277-155">12</span></span>     |        |
| <span data-ttu-id="cf277-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="cf277-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="cf277-157">12</span><span class="sxs-lookup"><span data-stu-id="cf277-157">12</span></span>     | <span data-ttu-id="cf277-158">12</span><span class="sxs-lookup"><span data-stu-id="cf277-158">12</span></span>     |        |
| <span data-ttu-id="cf277-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="cf277-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="cf277-160">16</span><span class="sxs-lookup"><span data-stu-id="cf277-160">16</span></span>     | <span data-ttu-id="cf277-161">16</span><span class="sxs-lookup"><span data-stu-id="cf277-161">16</span></span>     |        |
| <span data-ttu-id="cf277-162">intensidad de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="cf277-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="cf277-163">GL \_ INTENSITY4</span><span class="sxs-lookup"><span data-stu-id="cf277-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="cf277-164">4</span><span class="sxs-lookup"><span data-stu-id="cf277-164">4</span></span>      |
| <span data-ttu-id="cf277-165">GL \_ INTENSITY8</span><span class="sxs-lookup"><span data-stu-id="cf277-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="cf277-166">8</span><span class="sxs-lookup"><span data-stu-id="cf277-166">8</span></span>      |
| <span data-ttu-id="cf277-167">GL \_ INTENSITY12</span><span class="sxs-lookup"><span data-stu-id="cf277-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="cf277-168">12</span><span class="sxs-lookup"><span data-stu-id="cf277-168">12</span></span>     |
| <span data-ttu-id="cf277-169">GL \_ INTENSITY16</span><span class="sxs-lookup"><span data-stu-id="cf277-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="cf277-170">16</span><span class="sxs-lookup"><span data-stu-id="cf277-170">16</span></span>     |
| <span data-ttu-id="cf277-171">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="cf277-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="cf277-172">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="cf277-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="cf277-173">3</span><span class="sxs-lookup"><span data-stu-id="cf277-173">3</span></span>      | <span data-ttu-id="cf277-174">3</span><span class="sxs-lookup"><span data-stu-id="cf277-174">3</span></span>      | <span data-ttu-id="cf277-175">2</span><span class="sxs-lookup"><span data-stu-id="cf277-175">2</span></span>      |        |        |        |
| <span data-ttu-id="cf277-176">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="cf277-176">GL\_RGB4</span></span>                 | <span data-ttu-id="cf277-177">4</span><span class="sxs-lookup"><span data-stu-id="cf277-177">4</span></span>      | <span data-ttu-id="cf277-178">4</span><span class="sxs-lookup"><span data-stu-id="cf277-178">4</span></span>      | <span data-ttu-id="cf277-179">4</span><span class="sxs-lookup"><span data-stu-id="cf277-179">4</span></span>      |        |        |        |
| <span data-ttu-id="cf277-180">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="cf277-180">GL\_RGB5</span></span>                 | <span data-ttu-id="cf277-181">5</span><span class="sxs-lookup"><span data-stu-id="cf277-181">5</span></span>      | <span data-ttu-id="cf277-182">5</span><span class="sxs-lookup"><span data-stu-id="cf277-182">5</span></span>      | <span data-ttu-id="cf277-183">5</span><span class="sxs-lookup"><span data-stu-id="cf277-183">5</span></span>      |        |        |        |
| <span data-ttu-id="cf277-184">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="cf277-184">GL\_RGB8</span></span>                 | <span data-ttu-id="cf277-185">8</span><span class="sxs-lookup"><span data-stu-id="cf277-185">8</span></span>      | <span data-ttu-id="cf277-186">8</span><span class="sxs-lookup"><span data-stu-id="cf277-186">8</span></span>      | <span data-ttu-id="cf277-187">8</span><span class="sxs-lookup"><span data-stu-id="cf277-187">8</span></span>      |        |        |        |
| <span data-ttu-id="cf277-188">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="cf277-188">GL\_RGB10</span></span>                | <span data-ttu-id="cf277-189">10</span><span class="sxs-lookup"><span data-stu-id="cf277-189">10</span></span>     | <span data-ttu-id="cf277-190">10</span><span class="sxs-lookup"><span data-stu-id="cf277-190">10</span></span>     | <span data-ttu-id="cf277-191">10</span><span class="sxs-lookup"><span data-stu-id="cf277-191">10</span></span>     |        |        |        |
| <span data-ttu-id="cf277-192">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="cf277-192">GL\_RGB12</span></span>                | <span data-ttu-id="cf277-193">12</span><span class="sxs-lookup"><span data-stu-id="cf277-193">12</span></span>     | <span data-ttu-id="cf277-194">12</span><span class="sxs-lookup"><span data-stu-id="cf277-194">12</span></span>     | <span data-ttu-id="cf277-195">12</span><span class="sxs-lookup"><span data-stu-id="cf277-195">12</span></span>     |        |        |        |
| <span data-ttu-id="cf277-196">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="cf277-196">GL\_RGB16</span></span>                | <span data-ttu-id="cf277-197">16</span><span class="sxs-lookup"><span data-stu-id="cf277-197">16</span></span>     | <span data-ttu-id="cf277-198">16</span><span class="sxs-lookup"><span data-stu-id="cf277-198">16</span></span>     | <span data-ttu-id="cf277-199">16</span><span class="sxs-lookup"><span data-stu-id="cf277-199">16</span></span>     |        |        |        |
| <span data-ttu-id="cf277-200">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="cf277-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="cf277-201">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="cf277-201">GL\_RGBA2</span></span>                | <span data-ttu-id="cf277-202">2</span><span class="sxs-lookup"><span data-stu-id="cf277-202">2</span></span>      | <span data-ttu-id="cf277-203">2</span><span class="sxs-lookup"><span data-stu-id="cf277-203">2</span></span>      | <span data-ttu-id="cf277-204">2</span><span class="sxs-lookup"><span data-stu-id="cf277-204">2</span></span>      | <span data-ttu-id="cf277-205">2</span><span class="sxs-lookup"><span data-stu-id="cf277-205">2</span></span>      |        |        |
| <span data-ttu-id="cf277-206">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="cf277-206">GL\_RGBA4</span></span>                | <span data-ttu-id="cf277-207">4</span><span class="sxs-lookup"><span data-stu-id="cf277-207">4</span></span>      | <span data-ttu-id="cf277-208">4</span><span class="sxs-lookup"><span data-stu-id="cf277-208">4</span></span>      | <span data-ttu-id="cf277-209">4</span><span class="sxs-lookup"><span data-stu-id="cf277-209">4</span></span>      | <span data-ttu-id="cf277-210">4</span><span class="sxs-lookup"><span data-stu-id="cf277-210">4</span></span>      |        |        |
| <span data-ttu-id="cf277-211">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="cf277-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="cf277-212">5</span><span class="sxs-lookup"><span data-stu-id="cf277-212">5</span></span>      | <span data-ttu-id="cf277-213">5</span><span class="sxs-lookup"><span data-stu-id="cf277-213">5</span></span>      | <span data-ttu-id="cf277-214">5</span><span class="sxs-lookup"><span data-stu-id="cf277-214">5</span></span>      | <span data-ttu-id="cf277-215">1</span><span class="sxs-lookup"><span data-stu-id="cf277-215">1</span></span>      |        |        |
| <span data-ttu-id="cf277-216">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="cf277-216">GL\_RGBA8</span></span>                | <span data-ttu-id="cf277-217">8</span><span class="sxs-lookup"><span data-stu-id="cf277-217">8</span></span>      | <span data-ttu-id="cf277-218">8</span><span class="sxs-lookup"><span data-stu-id="cf277-218">8</span></span>      | <span data-ttu-id="cf277-219">8</span><span class="sxs-lookup"><span data-stu-id="cf277-219">8</span></span>      | <span data-ttu-id="cf277-220">8</span><span class="sxs-lookup"><span data-stu-id="cf277-220">8</span></span>      |        |        |
| <span data-ttu-id="cf277-221">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="cf277-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="cf277-222">10</span><span class="sxs-lookup"><span data-stu-id="cf277-222">10</span></span>     | <span data-ttu-id="cf277-223">10</span><span class="sxs-lookup"><span data-stu-id="cf277-223">10</span></span>     | <span data-ttu-id="cf277-224">10</span><span class="sxs-lookup"><span data-stu-id="cf277-224">10</span></span>     | <span data-ttu-id="cf277-225">2</span><span class="sxs-lookup"><span data-stu-id="cf277-225">2</span></span>      |        |        |
| <span data-ttu-id="cf277-226">GL \_ RGBA12</span><span class="sxs-lookup"><span data-stu-id="cf277-226">GL\_RGBA12</span></span>               | <span data-ttu-id="cf277-227">12</span><span class="sxs-lookup"><span data-stu-id="cf277-227">12</span></span>     | <span data-ttu-id="cf277-228">12</span><span class="sxs-lookup"><span data-stu-id="cf277-228">12</span></span>     | <span data-ttu-id="cf277-229">12</span><span class="sxs-lookup"><span data-stu-id="cf277-229">12</span></span>     | <span data-ttu-id="cf277-230">12</span><span class="sxs-lookup"><span data-stu-id="cf277-230">12</span></span>     |        |        |
| <span data-ttu-id="cf277-231">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="cf277-231">GL\_RGBA16</span></span>               | <span data-ttu-id="cf277-232">16</span><span class="sxs-lookup"><span data-stu-id="cf277-232">16</span></span>     | <span data-ttu-id="cf277-233">16</span><span class="sxs-lookup"><span data-stu-id="cf277-233">16</span></span>     | <span data-ttu-id="cf277-234">16</span><span class="sxs-lookup"><span data-stu-id="cf277-234">16</span></span>     | <span data-ttu-id="cf277-235">16</span><span class="sxs-lookup"><span data-stu-id="cf277-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="cf277-236">*x*</span><span class="sxs-lookup"><span data-stu-id="cf277-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-237">Coordenada x del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="cf277-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="cf277-238">*y*</span><span class="sxs-lookup"><span data-stu-id="cf277-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-239">Coordenada y del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="cf277-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="cf277-240">*width*</span><span class="sxs-lookup"><span data-stu-id="cf277-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-241">Ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="cf277-241">The width of the texture image.</span></span> <span data-ttu-id="cf277-242">Debe ser cero o 2N + 2 (*borde*) para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="cf277-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="cf277-243">El alto de la imagen de textura es 1.</span><span class="sxs-lookup"><span data-stu-id="cf277-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="cf277-244">*PDA*</span><span class="sxs-lookup"><span data-stu-id="cf277-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="cf277-245">Ancho del borde.</span><span class="sxs-lookup"><span data-stu-id="cf277-245">The width of the border.</span></span> <span data-ttu-id="cf277-246">Debe ser cero o 1.</span><span class="sxs-lookup"><span data-stu-id="cf277-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf277-247">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf277-247">Return value</span></span>

<span data-ttu-id="cf277-248">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cf277-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf277-249">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cf277-249">Error codes</span></span>

<span data-ttu-id="cf277-250">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="cf277-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cf277-251">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf277-251">Name</span></span>                                                                                                  | <span data-ttu-id="cf277-252">Significado</span><span class="sxs-lookup"><span data-stu-id="cf277-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf277-253"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cf277-254">el *destino* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="cf277-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="cf277-255"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cf277-256">el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cf277-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="cf277-257"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cf277-258">*Border* no era cero o 1.</span><span class="sxs-lookup"><span data-stu-id="cf277-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="cf277-259"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cf277-260">el *ancho* era menor que cero, mayor que 2 + \_ tamaño máximo de textura de GL \_ \_ o el *ancho* no se puede representar como 2n + (*Border*) para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="cf277-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="cf277-261"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cf277-262">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cf277-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="cf277-263">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf277-263">Remarks</span></span>

<span data-ttu-id="cf277-264">La función **glCopyTexImage1D** define una imagen de textura de una dimensión mediante píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="cf277-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="cf277-265">Mediante el nivel de mipmap especificado con el *nivel*, las matrices de texturas se definen como una fila de píxeles alineada con la esquina inferior izquierda de la ventana en las coordenadas especificadas por *x* *e y*, con una longitud *igual al* \* *borde*+ 2.</span><span class="sxs-lookup"><span data-stu-id="cf277-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="cf277-266">El formato interno de la matriz de textura se especifica con el parámetro *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="cf277-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="cf277-267">La función **glCopyTexImage1D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md), salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="cf277-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="cf277-268">El orden de los píxeles se determina con las coordenadas *x* inferiores correspondientes a las coordenadas de textura inferiores.</span><span class="sxs-lookup"><span data-stu-id="cf277-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="cf277-269">Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="cf277-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="cf277-270">No puede incluir llamadas a **glCopyTexImage1D** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="cf277-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="cf277-271">La función **glCopyTexImage1D** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cf277-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="cf277-272">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="cf277-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="cf277-273">Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="cf277-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="cf277-274">La siguiente función recupera información relacionada con **glCopyTexImage1D**:</span><span class="sxs-lookup"><span data-stu-id="cf277-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="cf277-275">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="cf277-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="cf277-276">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf277-276">Requirements</span></span>



| <span data-ttu-id="cf277-277">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf277-277">Requirement</span></span> | <span data-ttu-id="cf277-278">Value</span><span class="sxs-lookup"><span data-stu-id="cf277-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf277-279">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf277-279">Minimum supported client</span></span><br/> | <span data-ttu-id="cf277-280">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cf277-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cf277-281">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf277-281">Minimum supported server</span></span><br/> | <span data-ttu-id="cf277-282">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf277-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf277-283">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf277-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf277-284"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cf277-285">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf277-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf277-286"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf277-287">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf277-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf277-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf277-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf277-289">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf277-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf277-290">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="cf277-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="cf277-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cf277-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cf277-292">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="cf277-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="cf277-293">**glFog**</span><span class="sxs-lookup"><span data-stu-id="cf277-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="cf277-294">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="cf277-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="cf277-295">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="cf277-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="cf277-296">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="cf277-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="cf277-297">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="cf277-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="cf277-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="cf277-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="cf277-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cf277-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cf277-300">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="cf277-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





