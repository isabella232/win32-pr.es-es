---
title: función glCopyTexImage2D (GL. h)
description: La función glCopyTexImage2D copia píxeles de la fotogramas en una imagen de textura bidimensional.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D (función) OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905330"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="2dc5f-104">glCopyTexImage2D función)</span><span class="sxs-lookup"><span data-stu-id="2dc5f-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="2dc5f-105">La función **glCopyTexImage2D** copia píxeles de la fotogramas en una imagen de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc5f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dc5f-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="2dc5f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dc5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc5f-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-109">Destino al que se cambiarán los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="2dc5f-110">Debe tener el valor de la textura de contabilidad \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-111">*level*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-112">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-112">The level-of-detail number.</span></span> <span data-ttu-id="2dc5f-113">El nivel 0 es la imagen base.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-113">Level 0 is the base image.</span></span> <span data-ttu-id="2dc5f-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-116">El formato interno y la resolución de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="2dc5f-117">Los valores 1, 2, 3 y 4 no se aceptan para *internalFormat*.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="2dc5f-118">El parámetro puede suponer uno de los siguientes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="2dc5f-119">Constante</span><span class="sxs-lookup"><span data-stu-id="2dc5f-119">Constant</span></span>                 | <span data-ttu-id="2dc5f-120">Bits R</span><span class="sxs-lookup"><span data-stu-id="2dc5f-120">R Bits</span></span> | <span data-ttu-id="2dc5f-121">G bits</span><span class="sxs-lookup"><span data-stu-id="2dc5f-121">G Bits</span></span> | <span data-ttu-id="2dc5f-122">Bits B</span><span class="sxs-lookup"><span data-stu-id="2dc5f-122">B Bits</span></span> | <span data-ttu-id="2dc5f-123">Un bits</span><span class="sxs-lookup"><span data-stu-id="2dc5f-123">A Bits</span></span> | <span data-ttu-id="2dc5f-124">Bits L</span><span class="sxs-lookup"><span data-stu-id="2dc5f-124">L Bits</span></span> | <span data-ttu-id="2dc5f-125">I bits</span><span class="sxs-lookup"><span data-stu-id="2dc5f-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="2dc5f-126">libro \_ de contabilidad</span><span class="sxs-lookup"><span data-stu-id="2dc5f-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="2dc5f-127">GL \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="2dc5f-128">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-128">4</span></span>      |        |        |
| <span data-ttu-id="2dc5f-129">GL \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="2dc5f-130">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-130">8</span></span>      |        |        |
| <span data-ttu-id="2dc5f-131">GL \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="2dc5f-132">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-132">12</span></span>     |        |        |
| <span data-ttu-id="2dc5f-133">GL \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="2dc5f-134">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-134">16</span></span>     |        |        |
| <span data-ttu-id="2dc5f-135">luminancia del libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="2dc5f-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="2dc5f-136">GL \_ LUMINANCE4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="2dc5f-137">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-137">4</span></span>      |        |
| <span data-ttu-id="2dc5f-138">GL \_ LUMINANCE8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="2dc5f-139">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-139">8</span></span>      |        |
| <span data-ttu-id="2dc5f-140">GL \_ LUMINANCE12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="2dc5f-141">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-141">12</span></span>     |        |
| <span data-ttu-id="2dc5f-142">GL \_ LUMINANCE16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="2dc5f-143">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-143">16</span></span>     |        |
| <span data-ttu-id="2dc5f-144">alfa de luminancia de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="2dc5f-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="2dc5f-145">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="2dc5f-146">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-146">4</span></span>      | <span data-ttu-id="2dc5f-147">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-147">4</span></span>      |        |
| <span data-ttu-id="2dc5f-148">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="2dc5f-149">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-149">2</span></span>      | <span data-ttu-id="2dc5f-150">6</span><span class="sxs-lookup"><span data-stu-id="2dc5f-150">6</span></span>      |        |
| <span data-ttu-id="2dc5f-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="2dc5f-152">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-152">8</span></span>      | <span data-ttu-id="2dc5f-153">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-153">8</span></span>      |        |
| <span data-ttu-id="2dc5f-154">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="2dc5f-155">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-155">4</span></span>      | <span data-ttu-id="2dc5f-156">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-156">12</span></span>     |        |
| <span data-ttu-id="2dc5f-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="2dc5f-158">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-158">12</span></span>     | <span data-ttu-id="2dc5f-159">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-159">12</span></span>     |        |
| <span data-ttu-id="2dc5f-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="2dc5f-161">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-161">16</span></span>     | <span data-ttu-id="2dc5f-162">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-162">16</span></span>     |        |
| <span data-ttu-id="2dc5f-163">intensidad de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="2dc5f-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="2dc5f-164">GL \_ INTENSITY4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="2dc5f-165">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-165">4</span></span>      |
| <span data-ttu-id="2dc5f-166">GL \_ INTENSITY8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="2dc5f-167">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-167">8</span></span>      |
| <span data-ttu-id="2dc5f-168">GL \_ INTENSITY12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="2dc5f-169">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-169">12</span></span>     |
| <span data-ttu-id="2dc5f-170">GL \_ INTENSITY16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="2dc5f-171">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-171">16</span></span>     |
| <span data-ttu-id="2dc5f-172">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="2dc5f-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="2dc5f-173">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="2dc5f-174">3</span><span class="sxs-lookup"><span data-stu-id="2dc5f-174">3</span></span>      | <span data-ttu-id="2dc5f-175">3</span><span class="sxs-lookup"><span data-stu-id="2dc5f-175">3</span></span>      | <span data-ttu-id="2dc5f-176">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-176">2</span></span>      |        |        |        |
| <span data-ttu-id="2dc5f-177">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-177">GL\_RGB4</span></span>                 | <span data-ttu-id="2dc5f-178">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-178">4</span></span>      | <span data-ttu-id="2dc5f-179">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-179">4</span></span>      | <span data-ttu-id="2dc5f-180">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-180">4</span></span>      |        |        |        |
| <span data-ttu-id="2dc5f-181">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-181">GL\_RGB5</span></span>                 | <span data-ttu-id="2dc5f-182">5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-182">5</span></span>      | <span data-ttu-id="2dc5f-183">5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-183">5</span></span>      | <span data-ttu-id="2dc5f-184">5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-184">5</span></span>      |        |        |        |
| <span data-ttu-id="2dc5f-185">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-185">GL\_RGB8</span></span>                 | <span data-ttu-id="2dc5f-186">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-186">8</span></span>      | <span data-ttu-id="2dc5f-187">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-187">8</span></span>      | <span data-ttu-id="2dc5f-188">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-188">8</span></span>      |        |        |        |
| <span data-ttu-id="2dc5f-189">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-189">GL\_RGB10</span></span>                | <span data-ttu-id="2dc5f-190">10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-190">10</span></span>     | <span data-ttu-id="2dc5f-191">10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-191">10</span></span>     | <span data-ttu-id="2dc5f-192">10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-192">10</span></span>     |        |        |        |
| <span data-ttu-id="2dc5f-193">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-193">GL\_RGB12</span></span>                | <span data-ttu-id="2dc5f-194">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-194">12</span></span>     | <span data-ttu-id="2dc5f-195">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-195">12</span></span>     | <span data-ttu-id="2dc5f-196">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-196">12</span></span>     |        |        |        |
| <span data-ttu-id="2dc5f-197">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-197">GL\_RGB16</span></span>                | <span data-ttu-id="2dc5f-198">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-198">16</span></span>     | <span data-ttu-id="2dc5f-199">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-199">16</span></span>     | <span data-ttu-id="2dc5f-200">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-200">16</span></span>     |        |        |        |
| <span data-ttu-id="2dc5f-201">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="2dc5f-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="2dc5f-202">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-202">GL\_RGBA2</span></span>                | <span data-ttu-id="2dc5f-203">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-203">2</span></span>      | <span data-ttu-id="2dc5f-204">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-204">2</span></span>      | <span data-ttu-id="2dc5f-205">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-205">2</span></span>      | <span data-ttu-id="2dc5f-206">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-206">2</span></span>      |        |        |
| <span data-ttu-id="2dc5f-207">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-207">GL\_RGBA4</span></span>                | <span data-ttu-id="2dc5f-208">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-208">4</span></span>      | <span data-ttu-id="2dc5f-209">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-209">4</span></span>      | <span data-ttu-id="2dc5f-210">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-210">4</span></span>      | <span data-ttu-id="2dc5f-211">4</span><span class="sxs-lookup"><span data-stu-id="2dc5f-211">4</span></span>      |        |        |
| <span data-ttu-id="2dc5f-212">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="2dc5f-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="2dc5f-213">5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-213">5</span></span>      | <span data-ttu-id="2dc5f-214">5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-214">5</span></span>      | <span data-ttu-id="2dc5f-215">5</span><span class="sxs-lookup"><span data-stu-id="2dc5f-215">5</span></span>      | <span data-ttu-id="2dc5f-216">1</span><span class="sxs-lookup"><span data-stu-id="2dc5f-216">1</span></span>      |        |        |
| <span data-ttu-id="2dc5f-217">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-217">GL\_RGBA8</span></span>                | <span data-ttu-id="2dc5f-218">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-218">8</span></span>      | <span data-ttu-id="2dc5f-219">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-219">8</span></span>      | <span data-ttu-id="2dc5f-220">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-220">8</span></span>      | <span data-ttu-id="2dc5f-221">8</span><span class="sxs-lookup"><span data-stu-id="2dc5f-221">8</span></span>      |        |        |
| <span data-ttu-id="2dc5f-222">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="2dc5f-223">10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-223">10</span></span>     | <span data-ttu-id="2dc5f-224">10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-224">10</span></span>     | <span data-ttu-id="2dc5f-225">10</span><span class="sxs-lookup"><span data-stu-id="2dc5f-225">10</span></span>     | <span data-ttu-id="2dc5f-226">2</span><span class="sxs-lookup"><span data-stu-id="2dc5f-226">2</span></span>      |        |        |
| <span data-ttu-id="2dc5f-227">GL \_ RGBA12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-227">GL\_RGBA12</span></span>               | <span data-ttu-id="2dc5f-228">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-228">12</span></span>     | <span data-ttu-id="2dc5f-229">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-229">12</span></span>     | <span data-ttu-id="2dc5f-230">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-230">12</span></span>     | <span data-ttu-id="2dc5f-231">12</span><span class="sxs-lookup"><span data-stu-id="2dc5f-231">12</span></span>     |        |        |
| <span data-ttu-id="2dc5f-232">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-232">GL\_RGBA16</span></span>               | <span data-ttu-id="2dc5f-233">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-233">16</span></span>     | <span data-ttu-id="2dc5f-234">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-234">16</span></span>     | <span data-ttu-id="2dc5f-235">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-235">16</span></span>     | <span data-ttu-id="2dc5f-236">16</span><span class="sxs-lookup"><span data-stu-id="2dc5f-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="2dc5f-237">*x*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-238">Coordenada x del plano de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-239">*y*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-240">Coordenada y del plano de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-241">*width*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-242">Ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-242">The width of the texture image.</span></span> <span data-ttu-id="2dc5f-243">Debe ser un borde 2N + 2 \*  para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-244">*height*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-245">Alto de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-245">The height of the texture image.</span></span> <span data-ttu-id="2dc5f-246">Debe ser un borde 2N + 2 \*  para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-247">*PDA*</span><span class="sxs-lookup"><span data-stu-id="2dc5f-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc5f-248">Ancho del borde.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-248">The width of the border.</span></span> <span data-ttu-id="2dc5f-249">Debe ser cero o 1.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc5f-250">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dc5f-250">Return value</span></span>

<span data-ttu-id="2dc5f-251">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2dc5f-252">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2dc5f-252">Error codes</span></span>

<span data-ttu-id="2dc5f-253">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2dc5f-254">Nombre</span><span class="sxs-lookup"><span data-stu-id="2dc5f-254">Name</span></span>                                                                                                  | <span data-ttu-id="2dc5f-255">Significado</span><span class="sxs-lookup"><span data-stu-id="2dc5f-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dc5f-256"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2dc5f-257">el *destino* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="2dc5f-258"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2dc5f-259">el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2dc5f-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="2dc5f-260"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2dc5f-261">*Border* no era cero o 1.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="2dc5f-262"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2dc5f-263">el *ancho* era menor que cero, mayor que 2 + \_ tamaño máximo de textura de GL \_ \_ o el *ancho* no se puede representar como borde 2N + 2 \*  para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="2dc5f-264"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2dc5f-265">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2dc5f-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="2dc5f-266">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dc5f-266">Remarks</span></span>

<span data-ttu-id="2dc5f-267">La función **glCopyTexImage2D** define una imagen de textura bidimensional mediante píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="2dc5f-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="2dc5f-268">Mediante el nivel de mipmap especificado con el *nivel*, las matrices de textura se definen como un rectángulo de píxeles con la esquina inferior izquierda ubicada en las coordenadas *x* e *y*, el ancho es igual al *ancho* + (2 \* *borde*) y un alto igual a *alto* + (2 \* *borde*).</span><span class="sxs-lookup"><span data-stu-id="2dc5f-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="2dc5f-269">El formato interno de la matriz de textura se especifica con el parámetro *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="2dc5f-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="2dc5f-270">La función **glCopyTexImage2D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md) , salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="2dc5f-271">El orden de los píxeles se determina con las coordenadas *x* *e y* inferiores correspondientes a las coordenadas de textura *s* y *t* inferiores.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="2dc5f-272">Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="2dc5f-273">No puede incluir llamadas a **glCopyTexImage2D** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="2dc5f-274">La función **glCopyTexImage2D** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="2dc5f-275">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="2dc5f-276">Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="2dc5f-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="2dc5f-277">La siguiente función recupera información relacionada con **glCopyTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="2dc5f-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="2dc5f-278">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="2dc5f-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc5f-279">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dc5f-279">Requirements</span></span>



| <span data-ttu-id="2dc5f-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dc5f-280">Requirement</span></span> | <span data-ttu-id="2dc5f-281">Value</span><span class="sxs-lookup"><span data-stu-id="2dc5f-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc5f-282">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc5f-282">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc5f-283">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2dc5f-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2dc5f-284">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc5f-284">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc5f-285">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2dc5f-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2dc5f-286">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dc5f-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dc5f-287"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2dc5f-288">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2dc5f-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="2dc5f-289"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2dc5f-290">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2dc5f-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dc5f-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc5f-292">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dc5f-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc5f-293">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-295">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-296">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-297">**glFog**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-298">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-299">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-300">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-301">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-304">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





