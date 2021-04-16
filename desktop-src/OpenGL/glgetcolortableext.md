---
title: función glGetColorTableEXT (GL. h)
description: La función glGetColorTableEXT obtiene los datos de la tabla de colores de la paleta de texturas de destino actual.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glGetColorTableEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686250"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="8f4e0-104">glGetColorTableEXT función)</span><span class="sxs-lookup"><span data-stu-id="8f4e0-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="8f4e0-105">La función **glGetColorTableEXT** obtiene los datos de la tabla de colores de la paleta de texturas de destino actual.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f4e0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f4e0-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="8f4e0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f4e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f4e0-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="8f4e0-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4e0-109">Textura de destino que va a cambiar su paleta.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="8f4e0-110">Debe ser \_ de textura 1D o textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="8f4e0-111">*format*</span><span class="sxs-lookup"><span data-stu-id="8f4e0-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4e0-112">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-112">The format of the pixel data.</span></span> <span data-ttu-id="8f4e0-113">Se aceptan las siguientes constantes simbólicas.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f4e0-114">Value</span><span class="sxs-lookup"><span data-stu-id="8f4e0-114">Value</span></span></th>
<th><span data-ttu-id="8f4e0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8f4e0-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="8f4e0-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-117">Cada píxel es un grupo de cuatro componentes en el siguiente orden: rojo, verde, azul, alfa.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="8f4e0-118">El formato RGBA se determina de esta manera:</span><span class="sxs-lookup"><span data-stu-id="8f4e0-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="8f4e0-119">La función <strong>glGetColorTableEXT</strong> convierte los valores de punto flotante directamente a un formato interno con una precisión no especificada.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="8f4e0-120">Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor entero representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="8f4e0-121">Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="8f4e0-122">La función <strong>glGetColorTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="8f4e0-123">Los resultados se fijan en el intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="8f4e0-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="8f4e0-124">Si GL_MAP_COLOR es <strong>true</strong>, <strong>glGetColorTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="8f4e0-125">La función <strong>glGetColorTableEXT</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas z y de textura de la posición de la trama actual a cada píxel y asignando las coordenadas de la ventana <em>x</em> e <em>y</em> al fragmento <em>n</em>, tal que <em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="8f4e0-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="8f4e0-126"> = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="8f4e0-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="8f4e0-127">¿ <em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="8f4e0-127"><em>y</em>?</span></span><span data-ttu-id="8f4e0-128"> = <em></em><sub></sub> + <em>n/ancho</em> de r</span><span class="sxs-lookup"><span data-stu-id="8f4e0-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="8f4e0-129">donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="8f4e0-130">Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="8f4e0-131">La función <strong>glGetColorTableEXT</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="8f4e0-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-133">Cada píxel es un único componente rojo.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="8f4e0-134">La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA es, lo convierte en un píxel RGBA con el verde y el azul establecidos en 0,0 y el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="8f4e0-135">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="8f4e0-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-137">Cada píxel es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="8f4e0-138">La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo y el azul establecidos en 0,0 y el alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="8f4e0-139">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="8f4e0-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-141">Cada píxel es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="8f4e0-142">La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="8f4e0-143">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="8f4e0-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-145">Cada píxel es un único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="8f4e0-146">La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="8f4e0-147">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="8f4e0-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-149">Cada píxel es un grupo de tres componentes en este orden: rojo, verde, azul.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="8f4e0-150">La función <strong>glGetColorTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="8f4e0-151">El color triple se convierte en un píxel RGBA con el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="8f4e0-152">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="8f4e0-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-154">Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="8f4e0-155">GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="8f4e0-156">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="8f4e0-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f4e0-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8f4e0-158">Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="8f4e0-159">GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="8f4e0-160">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="8f4e0-161">*type*</span><span class="sxs-lookup"><span data-stu-id="8f4e0-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4e0-162">El tipo de datos para los *datos*.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-162">The data type for *data*.</span></span> <span data-ttu-id="8f4e0-163">A continuación se indican las constantes simbólicas aceptadas y su significado.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="8f4e0-164">Value</span><span class="sxs-lookup"><span data-stu-id="8f4e0-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="8f4e0-165">Significado</span><span class="sxs-lookup"><span data-stu-id="8f4e0-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="8f4e0-166"><dt>**\_byte sin signo de \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="8f4e0-167">Entero de 8 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="8f4e0-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="8f4e0-168"><dt>**BYTE de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="8f4e0-169">Entero de 8 bits con signo</span><span class="sxs-lookup"><span data-stu-id="8f4e0-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="8f4e0-170"><dt>**libro de contabilidad \_ corto sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="8f4e0-171">Entero de 16 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="8f4e0-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="8f4e0-172"><dt>**CONTABILIDAD \_ breve**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="8f4e0-173">Entero de 16 bits con signo</span><span class="sxs-lookup"><span data-stu-id="8f4e0-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="8f4e0-174"><dt>**libro de contabilidad \_ sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="8f4e0-175">Entero de 32 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="8f4e0-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="8f4e0-176"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="8f4e0-177">Entero de 32 bits</span><span class="sxs-lookup"><span data-stu-id="8f4e0-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="8f4e0-178"><dt>**valor \_ float de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="8f4e0-179">Valor de punto flotante de precisión sencilla</span><span class="sxs-lookup"><span data-stu-id="8f4e0-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f4e0-180">*data*</span><span class="sxs-lookup"><span data-stu-id="8f4e0-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4e0-181">Apunta a la ubicación donde se va a almacenar la información de la tabla de colores devuelta.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="8f4e0-182">Cada entrada de la tabla de colores se almacena como si fuera un solo píxel de una textura 1D.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="8f4e0-183">Dado que todas las texturas tienen una paleta predeterminada, **glGetColorTableEXT** siempre devuelve la información de la paleta aunque los datos de la textura no estén en un formato de paleta.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f4e0-184">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f4e0-184">Return value</span></span>

<span data-ttu-id="8f4e0-185">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8f4e0-186">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8f4e0-186">Error codes</span></span>

<span data-ttu-id="8f4e0-187">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8f4e0-188">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f4e0-188">Name</span></span>                                                                                                  | <span data-ttu-id="8f4e0-189">Significado</span><span class="sxs-lookup"><span data-stu-id="8f4e0-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f4e0-190"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8f4e0-191">*destino*, *formato* o *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="8f4e0-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="8f4e0-192"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8f4e0-193">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8f4e0-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8f4e0-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f4e0-194">Remarks</span></span>

<span data-ttu-id="8f4e0-195">La función **glGetColorTableEXT** obtiene los datos de la tabla de colores reales especificados por [**glColorTableEXT**](glcolortableext.md) y [**glColorSubTableEXT**](glcolorsubtableext.md).</span><span class="sxs-lookup"><span data-stu-id="8f4e0-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="8f4e0-196">La función **glGetColorTableEXT** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de textura de la paleta de GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8f4e0-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="8f4e0-197">Para comprobar si la implementación de OpenGL es compatible con **glGetColorTableEXT**, llame a [**glGetString**](glgetstring.md)(extensiones de GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="8f4e0-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="8f4e0-198">Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admite **glGetColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="8f4e0-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="8f4e0-199">Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="8f4e0-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f4e0-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f4e0-200">Requirements</span></span>



| <span data-ttu-id="8f4e0-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f4e0-201">Requirement</span></span> | <span data-ttu-id="8f4e0-202">Value</span><span class="sxs-lookup"><span data-stu-id="8f4e0-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8f4e0-203">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f4e0-203">Minimum supported client</span></span><br/> | <span data-ttu-id="8f4e0-204">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8f4e0-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="8f4e0-205">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f4e0-205">Minimum supported server</span></span><br/> | <span data-ttu-id="8f4e0-206">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f4e0-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8f4e0-207">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f4e0-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f4e0-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f4e0-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f4e0-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f4e0-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f4e0-210">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="8f4e0-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="8f4e0-211">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="8f4e0-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="8f4e0-212">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="8f4e0-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="8f4e0-213">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="8f4e0-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="8f4e0-214">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="8f4e0-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





