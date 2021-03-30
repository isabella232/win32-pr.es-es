---
title: función glColorTableEXT (GL. h)
description: La función glColorTableEXT especifica el formato y el tamaño de una paleta para las texturas de paletas de destino.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glColorTableEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802809"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="e4661-104">glColorTableEXT función)</span><span class="sxs-lookup"><span data-stu-id="e4661-104">glColorTableEXT function</span></span>

<span data-ttu-id="e4661-105">La función **glColorTableEXT** especifica el formato y el tamaño de una paleta para las texturas de paletas de destino.</span><span class="sxs-lookup"><span data-stu-id="e4661-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4661-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4661-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="e4661-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4661-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4661-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="e4661-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="e4661-109">Textura de destino que va a cambiar su paleta.</span><span class="sxs-lookup"><span data-stu-id="e4661-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="e4661-110">Debe ser la textura \_ 1D, textura \_ 2D, \_ textura de proxy \_ 1D o \_ textura de proxy \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="e4661-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="e4661-111">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="e4661-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e4661-112">El formato interno y la resolución de la paleta.</span><span class="sxs-lookup"><span data-stu-id="e4661-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="e4661-113">Este parámetro puede suponer uno de los siguientes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="e4661-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="e4661-114">Constante</span><span class="sxs-lookup"><span data-stu-id="e4661-114">Constant</span></span>       | <span data-ttu-id="e4661-115">Formato base</span><span class="sxs-lookup"><span data-stu-id="e4661-115">Base Format</span></span> | <span data-ttu-id="e4661-116">Bits R</span><span class="sxs-lookup"><span data-stu-id="e4661-116">R Bits</span></span> | <span data-ttu-id="e4661-117">G bits</span><span class="sxs-lookup"><span data-stu-id="e4661-117">G Bits</span></span> | <span data-ttu-id="e4661-118">Bits B</span><span class="sxs-lookup"><span data-stu-id="e4661-118">B Bits</span></span> | <span data-ttu-id="e4661-119">Un bits</span><span class="sxs-lookup"><span data-stu-id="e4661-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="e4661-120">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="e4661-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="e4661-121">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-121">GL\_RGB</span></span>     | <span data-ttu-id="e4661-122">3</span><span class="sxs-lookup"><span data-stu-id="e4661-122">3</span></span>      | <span data-ttu-id="e4661-123">3</span><span class="sxs-lookup"><span data-stu-id="e4661-123">3</span></span>      | <span data-ttu-id="e4661-124">2</span><span class="sxs-lookup"><span data-stu-id="e4661-124">2</span></span>      |        |
| <span data-ttu-id="e4661-125">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="e4661-125">GL\_RGB4</span></span>       | <span data-ttu-id="e4661-126">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-126">GL\_RGB</span></span>     | <span data-ttu-id="e4661-127">4</span><span class="sxs-lookup"><span data-stu-id="e4661-127">4</span></span>      | <span data-ttu-id="e4661-128">4</span><span class="sxs-lookup"><span data-stu-id="e4661-128">4</span></span>      | <span data-ttu-id="e4661-129">4</span><span class="sxs-lookup"><span data-stu-id="e4661-129">4</span></span>      |        |
| <span data-ttu-id="e4661-130">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="e4661-130">GL\_RGB5</span></span>       | <span data-ttu-id="e4661-131">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-131">GL\_RGB</span></span>     | <span data-ttu-id="e4661-132">5</span><span class="sxs-lookup"><span data-stu-id="e4661-132">5</span></span>      | <span data-ttu-id="e4661-133">5</span><span class="sxs-lookup"><span data-stu-id="e4661-133">5</span></span>      | <span data-ttu-id="e4661-134">5</span><span class="sxs-lookup"><span data-stu-id="e4661-134">5</span></span>      |        |
| <span data-ttu-id="e4661-135">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e4661-135">GL\_RGB8</span></span>       | <span data-ttu-id="e4661-136">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-136">GL\_RGB</span></span>     | <span data-ttu-id="e4661-137">8</span><span class="sxs-lookup"><span data-stu-id="e4661-137">8</span></span>      | <span data-ttu-id="e4661-138">8</span><span class="sxs-lookup"><span data-stu-id="e4661-138">8</span></span>      | <span data-ttu-id="e4661-139">8</span><span class="sxs-lookup"><span data-stu-id="e4661-139">8</span></span>      |        |
| <span data-ttu-id="e4661-140">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="e4661-140">GL\_RGB10</span></span>      | <span data-ttu-id="e4661-141">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-141">GL\_RGB</span></span>     | <span data-ttu-id="e4661-142">10</span><span class="sxs-lookup"><span data-stu-id="e4661-142">10</span></span>     | <span data-ttu-id="e4661-143">10</span><span class="sxs-lookup"><span data-stu-id="e4661-143">10</span></span>     | <span data-ttu-id="e4661-144">10</span><span class="sxs-lookup"><span data-stu-id="e4661-144">10</span></span>     |        |
| <span data-ttu-id="e4661-145">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="e4661-145">GL\_RGB12</span></span>      | <span data-ttu-id="e4661-146">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-146">GL\_RGB</span></span>     | <span data-ttu-id="e4661-147">12</span><span class="sxs-lookup"><span data-stu-id="e4661-147">12</span></span>     | <span data-ttu-id="e4661-148">12</span><span class="sxs-lookup"><span data-stu-id="e4661-148">12</span></span>     | <span data-ttu-id="e4661-149">12</span><span class="sxs-lookup"><span data-stu-id="e4661-149">12</span></span>     |        |
| <span data-ttu-id="e4661-150">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="e4661-150">GL\_RGB16</span></span>      | <span data-ttu-id="e4661-151">RGB de GL \_</span><span class="sxs-lookup"><span data-stu-id="e4661-151">GL\_RGB</span></span>     | <span data-ttu-id="e4661-152">16</span><span class="sxs-lookup"><span data-stu-id="e4661-152">16</span></span>     | <span data-ttu-id="e4661-153">16</span><span class="sxs-lookup"><span data-stu-id="e4661-153">16</span></span>     | <span data-ttu-id="e4661-154">16</span><span class="sxs-lookup"><span data-stu-id="e4661-154">16</span></span>     |        |
| <span data-ttu-id="e4661-155">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="e4661-155">GL\_RGBA2</span></span>      | <span data-ttu-id="e4661-156">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-156">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-157">2</span><span class="sxs-lookup"><span data-stu-id="e4661-157">2</span></span>      | <span data-ttu-id="e4661-158">2</span><span class="sxs-lookup"><span data-stu-id="e4661-158">2</span></span>      | <span data-ttu-id="e4661-159">2</span><span class="sxs-lookup"><span data-stu-id="e4661-159">2</span></span>      | <span data-ttu-id="e4661-160">2</span><span class="sxs-lookup"><span data-stu-id="e4661-160">2</span></span>      |
| <span data-ttu-id="e4661-161">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="e4661-161">GL\_RGBA4</span></span>      | <span data-ttu-id="e4661-162">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-162">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-163">4</span><span class="sxs-lookup"><span data-stu-id="e4661-163">4</span></span>      | <span data-ttu-id="e4661-164">4</span><span class="sxs-lookup"><span data-stu-id="e4661-164">4</span></span>      | <span data-ttu-id="e4661-165">4</span><span class="sxs-lookup"><span data-stu-id="e4661-165">4</span></span>      | <span data-ttu-id="e4661-166">4</span><span class="sxs-lookup"><span data-stu-id="e4661-166">4</span></span>      |
| <span data-ttu-id="e4661-167">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="e4661-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="e4661-168">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-168">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-169">5</span><span class="sxs-lookup"><span data-stu-id="e4661-169">5</span></span>      | <span data-ttu-id="e4661-170">5</span><span class="sxs-lookup"><span data-stu-id="e4661-170">5</span></span>      | <span data-ttu-id="e4661-171">5</span><span class="sxs-lookup"><span data-stu-id="e4661-171">5</span></span>      | <span data-ttu-id="e4661-172">1</span><span class="sxs-lookup"><span data-stu-id="e4661-172">1</span></span>      |
| <span data-ttu-id="e4661-173">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="e4661-173">GL\_RGBA8</span></span>      | <span data-ttu-id="e4661-174">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-174">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-175">8</span><span class="sxs-lookup"><span data-stu-id="e4661-175">8</span></span>      | <span data-ttu-id="e4661-176">8</span><span class="sxs-lookup"><span data-stu-id="e4661-176">8</span></span>      | <span data-ttu-id="e4661-177">8</span><span class="sxs-lookup"><span data-stu-id="e4661-177">8</span></span>      | <span data-ttu-id="e4661-178">8</span><span class="sxs-lookup"><span data-stu-id="e4661-178">8</span></span>      |
| <span data-ttu-id="e4661-179">GL \_ RG10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="e4661-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="e4661-180">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-180">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-181">10</span><span class="sxs-lookup"><span data-stu-id="e4661-181">10</span></span>     | <span data-ttu-id="e4661-182">10</span><span class="sxs-lookup"><span data-stu-id="e4661-182">10</span></span>     | <span data-ttu-id="e4661-183">10</span><span class="sxs-lookup"><span data-stu-id="e4661-183">10</span></span>     | <span data-ttu-id="e4661-184">2</span><span class="sxs-lookup"><span data-stu-id="e4661-184">2</span></span>      |
| <span data-ttu-id="e4661-185">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="e4661-185">GL\_RGB12</span></span>      | <span data-ttu-id="e4661-186">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-186">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-187">12</span><span class="sxs-lookup"><span data-stu-id="e4661-187">12</span></span>     | <span data-ttu-id="e4661-188">12</span><span class="sxs-lookup"><span data-stu-id="e4661-188">12</span></span>     | <span data-ttu-id="e4661-189">12</span><span class="sxs-lookup"><span data-stu-id="e4661-189">12</span></span>     | <span data-ttu-id="e4661-190">12</span><span class="sxs-lookup"><span data-stu-id="e4661-190">12</span></span>     |
| <span data-ttu-id="e4661-191">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="e4661-191">GL\_RGBA16</span></span>     | <span data-ttu-id="e4661-192">el \_ RGBA de GL</span><span class="sxs-lookup"><span data-stu-id="e4661-192">GL\_RGBA</span></span>    | <span data-ttu-id="e4661-193">16</span><span class="sxs-lookup"><span data-stu-id="e4661-193">16</span></span>     | <span data-ttu-id="e4661-194">16</span><span class="sxs-lookup"><span data-stu-id="e4661-194">16</span></span>     | <span data-ttu-id="e4661-195">16</span><span class="sxs-lookup"><span data-stu-id="e4661-195">16</span></span>     | <span data-ttu-id="e4661-196">16</span><span class="sxs-lookup"><span data-stu-id="e4661-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="e4661-197">*width*</span><span class="sxs-lookup"><span data-stu-id="e4661-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="e4661-198">Tamaño de la paleta.</span><span class="sxs-lookup"><span data-stu-id="e4661-198">The size of the palette.</span></span> <span data-ttu-id="e4661-199">Debe ser 2N = 1 para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="e4661-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="e4661-200">*format*</span><span class="sxs-lookup"><span data-stu-id="e4661-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="e4661-201">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="e4661-201">The format of the pixel data.</span></span> <span data-ttu-id="e4661-202">Se aceptan las siguientes constantes simbólicas.</span><span class="sxs-lookup"><span data-stu-id="e4661-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4661-203">Value</span><span class="sxs-lookup"><span data-stu-id="e4661-203">Value</span></span></th>
<th><span data-ttu-id="e4661-204">Significado</span><span class="sxs-lookup"><span data-stu-id="e4661-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="e4661-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-206">Cada píxel es un grupo de cuatro componentes en este orden: rojo, verde, azul, alfa.</span><span class="sxs-lookup"><span data-stu-id="e4661-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="e4661-207">El formato RGBA se determina de esta manera:</span><span class="sxs-lookup"><span data-stu-id="e4661-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="e4661-208">La función <strong>glColorTableEXT</strong> convierte los valores de punto flotante directamente a un formato interno con una precisión no especificada.</span><span class="sxs-lookup"><span data-stu-id="e4661-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="e4661-209">Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor entero representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="e4661-210">Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="e4661-211">La función <strong>glColorTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos.</span><span class="sxs-lookup"><span data-stu-id="e4661-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="e4661-212">Los resultados se fijan en el intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="e4661-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="e4661-213">Si GL_MAP_COLOR es <strong>true</strong>, <strong>glColorTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e4661-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="e4661-214">La función <strong>glColorTableEXT</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas <em>z</em>y de textura de la posición de la trama actual a cada píxel y asignando las coordenadas de la ventana <em>x</em> e <em>y</em> al fragmento <em>n</em>, tal que<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="e4661-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="e4661-215"> = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="e4661-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="e4661-216"><em></em>sí?</span><span class="sxs-lookup"><span data-stu-id="e4661-216"><em></em>y?</span></span><span data-ttu-id="e4661-217"> = <em></em><sub></sub> +<em>n/ancho</em> de r</span><span class="sxs-lookup"><span data-stu-id="e4661-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="e4661-218">donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="e4661-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="e4661-219">Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos.</span><span class="sxs-lookup"><span data-stu-id="e4661-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="e4661-220">La función <strong>glColorTableEXT</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e4661-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="e4661-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-222">Cada píxel es un único componente rojo.</span><span class="sxs-lookup"><span data-stu-id="e4661-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="e4661-223">La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA es, lo convierte en un píxel RGBA con el verde y el azul establecidos en 0,0 y el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="e4661-224">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="e4661-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="e4661-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-226">Cada píxel es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="e4661-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="e4661-227">La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo y el azul establecidos en 0,0 y el alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="e4661-228">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="e4661-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="e4661-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-230">Cada píxel es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="e4661-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="e4661-231">La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="e4661-232">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="e4661-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="e4661-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-234">Cada píxel es un único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="e4661-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="e4661-235">La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="e4661-236">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="e4661-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="e4661-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-238">Cada píxel es un grupo de tres componentes en este orden: rojo, verde, azul.</span><span class="sxs-lookup"><span data-stu-id="e4661-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="e4661-239">La función <strong>glColorTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="e4661-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="e4661-240">El color triple se convierte en un píxel RGBA con el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="e4661-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="e4661-241">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="e4661-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="e4661-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-243">Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.</span><span class="sxs-lookup"><span data-stu-id="e4661-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="e4661-244">GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="e4661-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="e4661-245">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e4661-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="e4661-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e4661-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e4661-247">Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.</span><span class="sxs-lookup"><span data-stu-id="e4661-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="e4661-248">GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="e4661-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="e4661-249">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e4661-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="e4661-250">*type*</span><span class="sxs-lookup"><span data-stu-id="e4661-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="e4661-251">El tipo de datos para los *datos*.</span><span class="sxs-lookup"><span data-stu-id="e4661-251">The data type for *data*.</span></span> <span data-ttu-id="e4661-252">Se aceptan las constantes simbólicas siguientes: \_ byte sin signo de GL \_ , GL \_ byte, GL \_ sin signo \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int y GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="e4661-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="e4661-253">En la tabla siguiente se resume el significado de las constantes válidas para el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="e4661-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="e4661-254">Value</span><span class="sxs-lookup"><span data-stu-id="e4661-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="e4661-255">Significado</span><span class="sxs-lookup"><span data-stu-id="e4661-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="e4661-256"><dt>**\_byte sin signo de \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="e4661-257">Entero de 8 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="e4661-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="e4661-258"><dt>**BYTE de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="e4661-259">Entero de 8 bits con signo</span><span class="sxs-lookup"><span data-stu-id="e4661-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="e4661-260"><dt>**libro de contabilidad \_ corto sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="e4661-261">Entero de 16 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="e4661-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="e4661-262"><dt>**CONTABILIDAD \_ breve**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="e4661-263">Entero de 16 bits con signo</span><span class="sxs-lookup"><span data-stu-id="e4661-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="e4661-264"><dt>**libro de contabilidad \_ sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="e4661-265">Entero de 32 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="e4661-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="e4661-266"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="e4661-267">Entero de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e4661-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="e4661-268"><dt>**valor \_ float de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="e4661-269">Valor de punto flotante de precisión sencilla</span><span class="sxs-lookup"><span data-stu-id="e4661-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e4661-270">*data*</span><span class="sxs-lookup"><span data-stu-id="e4661-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="e4661-271">Puntero a los datos de textura de la paleta.</span><span class="sxs-lookup"><span data-stu-id="e4661-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="e4661-272">Los datos se tratan como píxeles individuales de una entrada de la paleta de texturas 1D para una entrada de la paleta.</span><span class="sxs-lookup"><span data-stu-id="e4661-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4661-273">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4661-273">Return value</span></span>

<span data-ttu-id="e4661-274">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e4661-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4661-275">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e4661-275">Error codes</span></span>

<span data-ttu-id="e4661-276">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e4661-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e4661-277">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4661-277">Name</span></span>                                                                                                  | <span data-ttu-id="e4661-278">Significado</span><span class="sxs-lookup"><span data-stu-id="e4661-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4661-279"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e4661-280">el *ancho* era un entero no válido.</span><span class="sxs-lookup"><span data-stu-id="e4661-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="e4661-281"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e4661-282">el *destino*, *internalFormat*, *formato* o *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="e4661-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="e4661-283"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e4661-284">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e4661-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4661-285">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4661-285">Remarks</span></span>

<span data-ttu-id="e4661-286">Las texturas de paleta se definen con una paleta de colores y un conjunto de datos de imagen compuesto por índices para las entradas de color de una paleta (una tabla de colores).</span><span class="sxs-lookup"><span data-stu-id="e4661-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="e4661-287">La función **glColorTableEXT** especifica la paleta de textura de una textura de destino.</span><span class="sxs-lookup"><span data-stu-id="e4661-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="e4661-288">Toma los *datos* de la memoria y convierte los datos como si cada entrada de la paleta es un píxel individual de una textura 1D.</span><span class="sxs-lookup"><span data-stu-id="e4661-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="e4661-289">La función **glColorTableEXT** desempaqueta y convierte los datos y los convierte en un formato interno que coincida lo más posible con el *formato* especificado.</span><span class="sxs-lookup"><span data-stu-id="e4661-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="e4661-290">Si el *ancho* de una paleta es mayor que el intervalo de los índices de color de los datos de textura, algunas de las entradas de la paleta no se usan.</span><span class="sxs-lookup"><span data-stu-id="e4661-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="e4661-291">Si el *ancho* de una paleta es menor que el intervalo de los índices de color de los datos de textura, se omiten los bits más significativos de los datos de textura y solo se usa el número adecuado de bits del índice al obtener acceso a la paleta.</span><span class="sxs-lookup"><span data-stu-id="e4661-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="e4661-292">Cuando se especifica un *destino* de proxy mediante la \_ textura \_ 1D de proxy o \_ \_ la textura de proxy 2D, se cambia el tamaño de la paleta de la textura del proxy y se establecen sus parámetros, pero no se transfiere ni se obtiene acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="e4661-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="e4661-293">Cuando el parámetro de *destino* es \_ GL \_ proxy Texture \_ 1D o GL \_ proxy \_ Texture \_ 2D, y la implementación no admite los valores especificados para el *formato* o el *ancho*, **glColorTableEXT** puede generar un error al crear la tabla de colores solicitada.</span><span class="sxs-lookup"><span data-stu-id="e4661-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="e4661-294">En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero.</span><span class="sxs-lookup"><span data-stu-id="e4661-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="e4661-295">Puede determinar si OpenGL admite un formato y un tamaño de tabla de colores determinados mediante una llamada a **glColorTableEXT** con un destino de proxy y, a continuación, llamar a [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar si el parámetro de ancho coincide con el establecido por **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="e4661-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="e4661-296">Si el ancho recuperado es cero, se produce un error en la solicitud de tabla de colores por **glColorTable** .</span><span class="sxs-lookup"><span data-stu-id="e4661-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="e4661-297">Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con la textura \_ 1D o textura \_ 2D para establecer la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="e4661-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="e4661-298">La función **glColorTableEXT** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de textura de la paleta de GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e4661-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="e4661-299">Para comprobar si la implementación de OpenGL es compatible con **glColorTableEXT**, llame a [**glGetString**](glgetstring.md)(extensiones de GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="e4661-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="e4661-300">Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admite **glColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="e4661-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="e4661-301">Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="e4661-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="e4661-302">Para recuperar los datos de la tabla de colores reales especificados por la función **glColorTableEXT** , llame a [**glGetColorTableEXT**](glgetcolortableext.md).</span><span class="sxs-lookup"><span data-stu-id="e4661-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="e4661-303">Para recuperar los parámetros, como el *ancho* y el *formato*, de la tabla de colores especificada por la función **glColorTableEXT** , llame a la función **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT** .</span><span class="sxs-lookup"><span data-stu-id="e4661-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4661-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4661-304">Requirements</span></span>



| <span data-ttu-id="e4661-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4661-305">Requirement</span></span> | <span data-ttu-id="e4661-306">Value</span><span class="sxs-lookup"><span data-stu-id="e4661-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e4661-307">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4661-307">Minimum supported client</span></span><br/> | <span data-ttu-id="e4661-308">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4661-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="e4661-309">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4661-309">Minimum supported server</span></span><br/> | <span data-ttu-id="e4661-310">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4661-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e4661-311">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4661-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4661-312"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4661-313">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4661-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4661-314">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e4661-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e4661-315">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="e4661-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="e4661-316">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e4661-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e4661-317">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="e4661-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="e4661-318">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="e4661-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="e4661-319">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="e4661-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="e4661-320">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="e4661-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





