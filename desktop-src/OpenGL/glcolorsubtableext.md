---
title: función glColorSubTableEXT (GL. h)
description: La función glColorSubTableEXT especifica una parte de la paleta de la textura de destino que se va a reemplazar.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glColorSubTableEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905331"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="a11cd-104">glColorSubTableEXT función)</span><span class="sxs-lookup"><span data-stu-id="a11cd-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="a11cd-105">La función **glColorSubTableEXT** especifica una parte de la paleta de la textura de destino que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="a11cd-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11cd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a11cd-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="a11cd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a11cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11cd-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="a11cd-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a11cd-109">Textura de la paleta de destino que va a cambiar su paleta.</span><span class="sxs-lookup"><span data-stu-id="a11cd-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="a11cd-110">Debe ser \_ de textura 1D o textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="a11cd-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="a11cd-111">*start*</span><span class="sxs-lookup"><span data-stu-id="a11cd-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="a11cd-112">Entrada de índice de la paleta inicial de la paleta que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="a11cd-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="a11cd-113">*count*</span><span class="sxs-lookup"><span data-stu-id="a11cd-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="a11cd-114">Número de entradas de índice de la paleta que se van a cambiar empezando en el *Inicio*.</span><span class="sxs-lookup"><span data-stu-id="a11cd-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="a11cd-115">El parámetro *Count* determina el intervalo de entradas de índice de la paleta que se cambian.</span><span class="sxs-lookup"><span data-stu-id="a11cd-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="a11cd-116">*format*</span><span class="sxs-lookup"><span data-stu-id="a11cd-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="a11cd-117">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a11cd-117">The format of the pixel data.</span></span> <span data-ttu-id="a11cd-118">Se aceptan las siguientes constantes simbólicas.</span><span class="sxs-lookup"><span data-stu-id="a11cd-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a11cd-119">Value</span><span class="sxs-lookup"><span data-stu-id="a11cd-119">Value</span></span></th>
<th><span data-ttu-id="a11cd-120">Significado</span><span class="sxs-lookup"><span data-stu-id="a11cd-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="a11cd-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-122">Cada píxel es un grupo de cuatro componentes en el siguiente orden: rojo, verde, azul, alfa.</span><span class="sxs-lookup"><span data-stu-id="a11cd-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="a11cd-123">El formato RGBA se determina de esta manera:</span><span class="sxs-lookup"><span data-stu-id="a11cd-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="a11cd-124">La función <strong>glColorSubTableEXT</strong> convierte los valores de punto flotante directamente a un formato interno con una precisión no especificada.</span><span class="sxs-lookup"><span data-stu-id="a11cd-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="a11cd-125">Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="a11cd-126">Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="a11cd-127">La función <strong>glColorSubTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos.</span><span class="sxs-lookup"><span data-stu-id="a11cd-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="a11cd-128">Los resultados se fijan en el intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="a11cd-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="a11cd-129">Si GL_MAP_COLOR es <strong>true</strong>, <strong>glColorSubTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a11cd-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="a11cd-130">La función <strong>glColorSubTableEXT</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas <em>z</em>y de textura de la posición de la trama actual a cada píxel y asignando las coordenadas de la ventana <em>x</em> e <em>y</em> al fragmento <em>n</em>, tal que<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="a11cd-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="a11cd-131"> = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="a11cd-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="a11cd-132">¿ <em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="a11cd-132"><em>y</em>?</span></span><span data-ttu-id="a11cd-133"> = <em></em><sub></sub> +<em>n/ancho</em> de r</span><span class="sxs-lookup"><span data-stu-id="a11cd-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="a11cd-134">donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="a11cd-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="a11cd-135">Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos.</span><span class="sxs-lookup"><span data-stu-id="a11cd-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="a11cd-136">La función <strong>glColorSubTableEXT</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a11cd-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="a11cd-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-138">Cada píxel es un único componente rojo.</span><span class="sxs-lookup"><span data-stu-id="a11cd-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="a11cd-139">La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA es, lo convierte en un píxel RGBA con el verde y el azul establecidos en 0,0 y el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="a11cd-140">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="a11cd-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="a11cd-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-142">Cada píxel es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="a11cd-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="a11cd-143">La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo y el azul establecidos en 0,0 y el alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="a11cd-144">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="a11cd-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="a11cd-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-146">Cada píxel es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="a11cd-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="a11cd-147">La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="a11cd-148">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="a11cd-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="a11cd-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-150">Cada píxel es un único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="a11cd-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="a11cd-151">La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="a11cd-152">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="a11cd-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="a11cd-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-154">Cada píxel es un grupo de tres componentes en este orden: rojo, verde, azul.</span><span class="sxs-lookup"><span data-stu-id="a11cd-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="a11cd-155">La función <strong>glColorSubTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="a11cd-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="a11cd-156">El color triple se convierte en un píxel RGBA con el valor alfa establecido en 1,0.</span><span class="sxs-lookup"><span data-stu-id="a11cd-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="a11cd-157">Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.</span><span class="sxs-lookup"><span data-stu-id="a11cd-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="a11cd-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-159">Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.</span><span class="sxs-lookup"><span data-stu-id="a11cd-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="a11cd-160">GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="a11cd-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a11cd-161">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a11cd-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="a11cd-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a11cd-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a11cd-163">Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.</span><span class="sxs-lookup"><span data-stu-id="a11cd-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="a11cd-164">GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="a11cd-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a11cd-165">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a11cd-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="a11cd-166">*type*</span><span class="sxs-lookup"><span data-stu-id="a11cd-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="a11cd-167">El tipo de datos para los *datos*.</span><span class="sxs-lookup"><span data-stu-id="a11cd-167">The data type for *data*.</span></span> <span data-ttu-id="a11cd-168">Se aceptan las constantes simbólicas siguientes: \_ byte sin signo de GL \_ , GL \_ byte, GL \_ sin signo \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int y GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="a11cd-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="a11cd-169">En la tabla siguiente se resume el significado de las constantes válidas para el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="a11cd-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="a11cd-170">Value</span><span class="sxs-lookup"><span data-stu-id="a11cd-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="a11cd-171">Significado</span><span class="sxs-lookup"><span data-stu-id="a11cd-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="a11cd-172"><dt>**\_byte sin signo de \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="a11cd-173">Entero de 8 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="a11cd-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="a11cd-174"><dt>**BYTE de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="a11cd-175">Entero de 8 bits con signo</span><span class="sxs-lookup"><span data-stu-id="a11cd-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="a11cd-176"><dt>**libro de contabilidad \_ corto sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="a11cd-177">Entero de 16 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="a11cd-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="a11cd-178"><dt>**CONTABILIDAD \_ breve**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="a11cd-179">Entero de 16 bits con signo</span><span class="sxs-lookup"><span data-stu-id="a11cd-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="a11cd-180"><dt>**libro de contabilidad \_ sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="a11cd-181">Entero de 32 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="a11cd-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="a11cd-182"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="a11cd-183">Entero de 32 bits</span><span class="sxs-lookup"><span data-stu-id="a11cd-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="a11cd-184"><dt>**valor \_ float de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="a11cd-185">Valor de punto flotante de precisión sencilla</span><span class="sxs-lookup"><span data-stu-id="a11cd-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a11cd-186">*data*</span><span class="sxs-lookup"><span data-stu-id="a11cd-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="a11cd-187">Puntero a los datos de textura de la paleta.</span><span class="sxs-lookup"><span data-stu-id="a11cd-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="a11cd-188">Los datos se tratan como píxeles individuales de una entrada de la paleta de texturas 1D para una entrada de la paleta.</span><span class="sxs-lookup"><span data-stu-id="a11cd-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11cd-189">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a11cd-189">Return value</span></span>

<span data-ttu-id="a11cd-190">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a11cd-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a11cd-191">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a11cd-191">Error codes</span></span>

<span data-ttu-id="a11cd-192">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a11cd-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a11cd-193">Nombre</span><span class="sxs-lookup"><span data-stu-id="a11cd-193">Name</span></span>                                                                                              | <span data-ttu-id="a11cd-194">Significado</span><span class="sxs-lookup"><span data-stu-id="a11cd-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a11cd-195"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="a11cd-196">*Start* o *Count* era un entero no válido.</span><span class="sxs-lookup"><span data-stu-id="a11cd-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a11cd-197"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="a11cd-198">*destino*, *formato* o *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="a11cd-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="a11cd-199"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="a11cd-200">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a11cd-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a11cd-201">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a11cd-201">Remarks</span></span>

<span data-ttu-id="a11cd-202">La función **glColorSubTableEXT** especifica partes de la paleta de la textura de destino actual que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="a11cd-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="a11cd-203">A diferencia de [**glColorTableEXT**](glcolortableext.md), no puede especificar que el parámetro de *destino* sea una paleta de texturas de proxy.</span><span class="sxs-lookup"><span data-stu-id="a11cd-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="a11cd-204">La función **glColorSubTableEXT** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de textura de la paleta de GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a11cd-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="a11cd-205">Para comprobar si la implementación de OpenGL es compatible con **glColorSubTableEXT**, llame a [**glGetString**](glgetstring.md)(extensiones de GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="a11cd-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="a11cd-206">Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admite **glColorSubTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="a11cd-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="a11cd-207">Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="a11cd-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a11cd-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a11cd-208">Requirements</span></span>



| <span data-ttu-id="a11cd-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11cd-209">Requirement</span></span> | <span data-ttu-id="a11cd-210">Value</span><span class="sxs-lookup"><span data-stu-id="a11cd-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a11cd-211">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a11cd-211">Minimum supported client</span></span><br/> | <span data-ttu-id="a11cd-212">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a11cd-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a11cd-213">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a11cd-213">Minimum supported server</span></span><br/> | <span data-ttu-id="a11cd-214">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a11cd-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a11cd-215">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a11cd-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="a11cd-216"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a11cd-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="a11cd-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11cd-218">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a11cd-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a11cd-219">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="a11cd-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="a11cd-220">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a11cd-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a11cd-221">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="a11cd-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="a11cd-222">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="a11cd-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="a11cd-223">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="a11cd-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="a11cd-224">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="a11cd-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="a11cd-225">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="a11cd-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





