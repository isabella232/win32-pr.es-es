---
title: función glCopyPixels (GL. h)
description: La función glCopyPixels copia píxeles en el fotogramas.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels (función) OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996526"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="52b06-104">glCopyPixels función)</span><span class="sxs-lookup"><span data-stu-id="52b06-104">glCopyPixels function</span></span>

<span data-ttu-id="52b06-105">La función **glCopyPixels** copia píxeles en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="52b06-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b06-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52b06-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="52b06-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52b06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52b06-108">*x*</span><span class="sxs-lookup"><span data-stu-id="52b06-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="52b06-109">Coordenada x del plano de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="52b06-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="52b06-110">*y*</span><span class="sxs-lookup"><span data-stu-id="52b06-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="52b06-111">Coordenada y del plano de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="52b06-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="52b06-112">*width*</span><span class="sxs-lookup"><span data-stu-id="52b06-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="52b06-113">Dimensión de ancho de la región rectangular de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="52b06-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="52b06-114">No debe ser negativo.</span><span class="sxs-lookup"><span data-stu-id="52b06-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="52b06-115">*height*</span><span class="sxs-lookup"><span data-stu-id="52b06-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="52b06-116">La dimensión de alto de la región rectangular de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="52b06-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="52b06-117">No debe ser negativo.</span><span class="sxs-lookup"><span data-stu-id="52b06-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="52b06-118">*type*</span><span class="sxs-lookup"><span data-stu-id="52b06-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="52b06-119">Especifica si **glCopyPixels** es copiar valores de color, valores de profundidad o valores de estarcido.</span><span class="sxs-lookup"><span data-stu-id="52b06-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="52b06-120">Las constantes simbólicas aceptables son.</span><span class="sxs-lookup"><span data-stu-id="52b06-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52b06-121">Value</span><span class="sxs-lookup"><span data-stu-id="52b06-121">Value</span></span></th>
<th><span data-ttu-id="52b06-122">Significado</span><span class="sxs-lookup"><span data-stu-id="52b06-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="52b06-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="52b06-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="52b06-124">La función <strong>glCopyPixels</strong> Lee índices o colores RGBA del búfer especificado actualmente como búfer de origen de lectura (vea <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="52b06-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="52b06-125">Si OpenGL está en modo de índice de color:</span><span class="sxs-lookup"><span data-stu-id="52b06-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="52b06-126">Cada índice que se lee desde este búfer se convierte en un formato de punto fijo con un número no especificado de bits a la derecha del punto binario.</span><span class="sxs-lookup"><span data-stu-id="52b06-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="52b06-127">Cada índice se desplaza a la izquierda GL_INDEX_SHIFT bits y se agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento está a la derecha.</span><span class="sxs-lookup"><span data-stu-id="52b06-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="52b06-128">En cualquier caso, cero bits rellenan de otro modo las ubicaciones de bits no especificadas en el resultado.</span><span class="sxs-lookup"><span data-stu-id="52b06-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="52b06-129">Si GL_MAP_COLOR es true, el índice se reemplaza por el valor al que hace referencia en la tabla de búsqueda GL_PIXEL_MAP_I_TO_I.</span><span class="sxs-lookup"><span data-stu-id="52b06-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="52b06-130">Tanto si el reemplazo de búsqueda del índice se realiza como si no, la parte entera del índice es then <strong>y</strong>Ed con 2<em><sup>b</sup></em> 1, donde <em>b</em> es el número de bits de un búfer de índice de color.</span><span class="sxs-lookup"><span data-stu-id="52b06-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="52b06-131">Si OpenGL está en modo RGBA:</span><span class="sxs-lookup"><span data-stu-id="52b06-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="52b06-132">Los componentes rojo, verde, azul y alfa de cada píxel que se lee se convierten a un formato de punto flotante interno con una precisión no especificada.</span><span class="sxs-lookup"><span data-stu-id="52b06-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="52b06-133">La conversión asigna el mayor valor de componente representable a 1,0 y el valor de componente de cero a 0,0.</span><span class="sxs-lookup"><span data-stu-id="52b06-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="52b06-134">Los valores de color de punto flotante resultantes se multiplican por GL_c_SCALE y se agregan a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos.</span><span class="sxs-lookup"><span data-stu-id="52b06-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="52b06-135">Los resultados se fijan en el intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="52b06-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="52b06-136">Si GL_MAP_COLOR es true, cada componente de color se escala según el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, se reemplaza por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="52b06-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="52b06-137">Los índices resultantes o los colores RGBA se convierten a fragmentos adjuntando las coordenadas <em>z</em>y de textura actuales de la posición de la línea de rasterizada a cada píxel y asignando después coordenadas de ventana (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual y el píxel era el <em></em> píxel en la posición <em>i</em></span><span class="sxs-lookup"><span data-stu-id="52b06-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="52b06-138">Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos.</span><span class="sxs-lookup"><span data-stu-id="52b06-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="52b06-139">La asignación de texturas, la niebla y todas las operaciones de fragmento se aplican antes de que los fragmentos se escriban en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="52b06-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="52b06-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="52b06-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="52b06-141">Los valores de profundidad se leen desde el búfer de profundidad y se convierten directamente a un formato de punto flotante interno con una precisión no especificada.</span><span class="sxs-lookup"><span data-stu-id="52b06-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="52b06-142">A continuación, el valor de profundidad de punto flotante resultante se multiplica por GL_DEPTH_SCALE y se agrega a GL_DEPTH_BIAS.</span><span class="sxs-lookup"><span data-stu-id="52b06-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="52b06-143">El resultado se fija en el intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="52b06-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="52b06-144">Los componentes de profundidad resultantes se convierten a fragmentos adjuntando el color de posición de la trama actual o el índice de color y las coordenadas de textura a cada píxel, asignando después coordenadas de ventana (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual y el <em></em> píxel era el píxel de la posición <em>i</em></span><span class="sxs-lookup"><span data-stu-id="52b06-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="52b06-145">Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos.</span><span class="sxs-lookup"><span data-stu-id="52b06-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="52b06-146">La asignación de texturas, la niebla y todas las operaciones de fragmento se aplican antes de que los fragmentos se escriban en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="52b06-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="52b06-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="52b06-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="52b06-148">Los índices de estarcido se leen desde el búfer de estarcido y se convierten a un formato de punto fijo interno con un número no especificado de bits a la derecha del punto binario.</span><span class="sxs-lookup"><span data-stu-id="52b06-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="52b06-149">A continuación, cada índice de punto fijo se desplaza a la izquierda GL_INDEX_SHIFT bits y se agrega a GL_INDEX_OFFSET.</span><span class="sxs-lookup"><span data-stu-id="52b06-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="52b06-150">Si GL_INDEX_SHIFT es negativo, el desplazamiento está a la derecha.</span><span class="sxs-lookup"><span data-stu-id="52b06-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="52b06-151">En cualquier caso, cero bits rellenan de otro modo las ubicaciones de bits no especificadas en el resultado.</span><span class="sxs-lookup"><span data-stu-id="52b06-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="52b06-152">Si GL_MAP_STENCIL es true, el índice se reemplaza por el valor al que hace referencia en la tabla de búsqueda GL_PIXEL_MAP_S_TO_S.</span><span class="sxs-lookup"><span data-stu-id="52b06-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="52b06-153">Tanto si el reemplazo de búsqueda del índice se realiza como si no, la parte entera del índice es entonces <strong>y</strong>Ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="52b06-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="52b06-154">Los índices de estarcido resultantes se escriben en el búfer de la galería de símbolos, de modo que el índice leído desde la ubicación <em>i</em> de la fila <em>j</em> se escribe en la ubicación (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="52b06-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="52b06-155">Solo la prueba de propiedad de píxeles, la prueba de tijera y la galería de símbolos writemask afectan a estas escrituras.</span><span class="sxs-lookup"><span data-stu-id="52b06-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52b06-156">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52b06-156">Return value</span></span>

<span data-ttu-id="52b06-157">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="52b06-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52b06-158">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="52b06-158">Error codes</span></span>

<span data-ttu-id="52b06-159">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="52b06-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="52b06-160">Nombre</span><span class="sxs-lookup"><span data-stu-id="52b06-160">Name</span></span>                                                                                                  | <span data-ttu-id="52b06-161">Significado</span><span class="sxs-lookup"><span data-stu-id="52b06-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52b06-162"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="52b06-163">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="52b06-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="52b06-164"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="52b06-165">El *ancho* o el alto era negativo.</span><span class="sxs-lookup"><span data-stu-id="52b06-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="52b06-166"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="52b06-167">el *tipo* era \_ profundidad de libro de contabilidad y no había ningún búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="52b06-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="52b06-168"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="52b06-169">el *tipo* es la \_ Galería de símbolos GL y no hay ningún búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="52b06-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="52b06-170"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="52b06-171">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="52b06-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="52b06-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52b06-172">Remarks</span></span>

<span data-ttu-id="52b06-173">La función **glCopyPixels** copia un rectángulo alineado en la pantalla de píxeles desde la ubicación fotogramas especificada a una región relativa a la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="52b06-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="52b06-174">Su funcionamiento está bien definido solo si toda la región de origen de píxeles está dentro de la parte expuesta de la ventana.</span><span class="sxs-lookup"><span data-stu-id="52b06-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="52b06-175">Los resultados de las copias desde fuera de la ventana de, o desde las regiones de la ventana que no están expuestas, dependen del hardware y no están definidas.</span><span class="sxs-lookup"><span data-stu-id="52b06-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="52b06-176">Los  parámetros x *e y* especifican las coordenadas de la ventana de la esquina inferior izquierda de la región rectangular que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="52b06-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="52b06-177">Los parámetros de *ancho* y *alto* especifican las dimensiones de la región rectangular que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="52b06-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="52b06-178">*Width* y *height* no deben ser negativos.</span><span class="sxs-lookup"><span data-stu-id="52b06-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="52b06-179">Varios parámetros controlan el procesamiento de los datos de píxeles mientras se copian.</span><span class="sxs-lookup"><span data-stu-id="52b06-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="52b06-180">Estos parámetros se establecen con tres funciones: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)y [**glPixelZoom**](glpixelzoom.md).</span><span class="sxs-lookup"><span data-stu-id="52b06-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="52b06-181">En este tema se describen los efectos de **glCopyPixels** de la mayoría de los parámetros especificados por estas tres funciones, pero no todos.</span><span class="sxs-lookup"><span data-stu-id="52b06-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="52b06-182">La función **glCopyPixels** copia los valores de cada píxel con la esquina inferior izquierda en (*x*  +  *i*, *y*  +  *j*) para 0 = *i*  <  *width* y 0 = *j*  <  *height*.</span><span class="sxs-lookup"><span data-stu-id="52b06-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="52b06-183">Este píxel se dice que es el píxel *i* de la fila *j* .</span><span class="sxs-lookup"><span data-stu-id="52b06-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="52b06-184">Los píxeles se copian en orden de fila desde la fila más baja hasta la más alta, de izquierda a derecha en cada fila.</span><span class="sxs-lookup"><span data-stu-id="52b06-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="52b06-185">El parámetro de *tipo* especifica si se copiarán los datos de color, profundidad o estarcido.</span><span class="sxs-lookup"><span data-stu-id="52b06-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="52b06-186">La rasterización descrita hasta ahora supone un factor de zoom de píxeles de 1,0.</span><span class="sxs-lookup"><span data-stu-id="52b06-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="52b06-187">Si usa [**glPixelZoom**](glpixelzoom.md) para cambiar los factores de zoom de píxeles *x* *e y, los píxeles se* convierten en fragmentos como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="52b06-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="52b06-188">Si (*x*<sub>r</sub> , *y*<sub>r</sub> ) es la posición de la trama actual y un píxel determinado está en la ubicación *i* de la fila *j* del rectángulo de píxeles de origen, se generan fragmentos para los píxeles cuyos centros se encuentran en el rectángulo con esquinas en</span><span class="sxs-lookup"><span data-stu-id="52b06-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="52b06-189">(*x*<sub>r</sub>  +  ¿ *zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*</span><span class="sxs-lookup"><span data-stu-id="52b06-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="52b06-190">y</span><span class="sxs-lookup"><span data-stu-id="52b06-190">and</span></span>

<span data-ttu-id="52b06-191">(*x*<sub>r</sub>  +  ¿ *zoom*?</span><span class="sxs-lookup"><span data-stu-id="52b06-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="52b06-192">(*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))</span><span class="sxs-lookup"><span data-stu-id="52b06-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="52b06-193">¿Dónde *hacer zoom*? es el valor de zoom de GL \_ \_ X y *zoom*<sub>y</sub> es el valor de zoom de GL \_ \_ y.</span><span class="sxs-lookup"><span data-stu-id="52b06-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="52b06-194">Los modos especificados por [**glPixelStore**](glpixelstore-functions.md) no tienen ningún efecto en el funcionamiento de **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="52b06-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="52b06-195">Las siguientes funciones recuperan información relacionada con **glCopyPixels**:</span><span class="sxs-lookup"><span data-stu-id="52b06-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="52b06-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="52b06-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="52b06-197">**glGet** con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido</span><span class="sxs-lookup"><span data-stu-id="52b06-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="52b06-198">Para copiar el píxel de color en la esquina inferior izquierda de la ventana a la posición de la trama actual, use</span><span class="sxs-lookup"><span data-stu-id="52b06-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="52b06-199">**glCopyPixels**(0, 0, 1, 1, color de GL \_ );</span><span class="sxs-lookup"><span data-stu-id="52b06-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="52b06-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52b06-200">Requirements</span></span>



| <span data-ttu-id="52b06-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="52b06-201">Requirement</span></span> | <span data-ttu-id="52b06-202">Value</span><span class="sxs-lookup"><span data-stu-id="52b06-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52b06-203">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52b06-203">Minimum supported client</span></span><br/> | <span data-ttu-id="52b06-204">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52b06-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="52b06-205">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52b06-205">Minimum supported server</span></span><br/> | <span data-ttu-id="52b06-206">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52b06-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52b06-207">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52b06-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="52b06-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="52b06-209">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52b06-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="52b06-210"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="52b06-211">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52b06-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52b06-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52b06-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52b06-213">Vea también</span><span class="sxs-lookup"><span data-stu-id="52b06-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b06-214">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="52b06-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="52b06-215">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="52b06-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="52b06-216">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="52b06-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="52b06-217">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="52b06-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="52b06-218">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="52b06-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="52b06-219">**glGet**</span><span class="sxs-lookup"><span data-stu-id="52b06-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="52b06-220">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="52b06-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="52b06-221">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="52b06-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="52b06-222">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="52b06-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="52b06-223">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="52b06-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="52b06-224">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="52b06-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="52b06-225">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="52b06-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="52b06-226">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="52b06-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="52b06-227">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="52b06-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





