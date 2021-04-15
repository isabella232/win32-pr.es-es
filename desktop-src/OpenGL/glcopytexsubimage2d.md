---
title: función glCopyTexSubImage2D (GL. h)
description: La función glCopyTexSubImage2D copia una subimagen de una imagen de textura bidimensional a partir de fotogramas.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D (función) OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422393"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="9389c-104">glCopyTexSubImage2D función)</span><span class="sxs-lookup"><span data-stu-id="9389c-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="9389c-105">La función **glCopyTexSubImage2D** copia una subimagen de una imagen de textura bidimensional a partir de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9389c-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9389c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9389c-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="9389c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9389c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9389c-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="9389c-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-109">Destino al que se cambiarán los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="9389c-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="9389c-110">Debe tener el valor de la textura de contabilidad \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="9389c-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-111">*level*</span><span class="sxs-lookup"><span data-stu-id="9389c-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-112">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="9389c-112">The level-of-detail number.</span></span> <span data-ttu-id="9389c-113">El nivel 0 es la imagen base.</span><span class="sxs-lookup"><span data-stu-id="9389c-113">Level 0 is the base image.</span></span> <span data-ttu-id="9389c-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="9389c-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="9389c-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-116">Desplazamiento textura en la dirección *x* dentro de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-117">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="9389c-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-118">El desplazamiento textura en la dirección *y* dentro de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="9389c-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-120">Coordenadas de plano x de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="9389c-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-121">*y*</span><span class="sxs-lookup"><span data-stu-id="9389c-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-122">Coordenadas y del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="9389c-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-123">*width*</span><span class="sxs-lookup"><span data-stu-id="9389c-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-124">Ancho de la subimagen de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="9389c-125">Especificar una subimagen de textura con un ancho de cero no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="9389c-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="9389c-126">*height*</span><span class="sxs-lookup"><span data-stu-id="9389c-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="9389c-127">Alto de la imagen secundaria de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="9389c-128">Especificar una subimagen de textura con un ancho de cero no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="9389c-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9389c-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9389c-129">Return value</span></span>

<span data-ttu-id="9389c-130">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9389c-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9389c-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9389c-131">Error codes</span></span>

<span data-ttu-id="9389c-132">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="9389c-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9389c-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="9389c-133">Name</span></span>                                                                                                  | <span data-ttu-id="9389c-134">Significado</span><span class="sxs-lookup"><span data-stu-id="9389c-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9389c-135"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9389c-136">el *destino* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="9389c-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="9389c-137"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9389c-138">el *nivel* era menor que cero o mayor que el *registro* 2 (*Max*), donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9389c-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="9389c-139"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9389c-140">*xoffset* era menor que *Border* o (*el*  +  *ancho* de xoffset) era mayor que (*w*  +  *Border*), *YOFFSET* era menor que *Border*, o (el alto de *YOFFSET*  +  ) era mayor que (  +  *borde* h), donde *w* es el \_ \_ ancho y el *borde* de la textura de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9389c-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="9389c-141">Tenga en cuenta que *w* incluye dos veces el ancho del *borde* .</span><span class="sxs-lookup"><span data-stu-id="9389c-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="9389c-142"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9389c-143">el *ancho* era menor *que Border* o *y* era menor que *Border*, donde *Border* es el ancho del borde de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="9389c-144"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9389c-145">Una operación [**glTexImage1D**](glteximage1d.md) anterior no definió la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="9389c-146"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9389c-147">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9389c-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="9389c-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9389c-148">Remarks</span></span>

<span data-ttu-id="9389c-149">La función **glCopyTexSubImage2D** reemplaza una parte rectangular de una imagen de textura bidimensional con píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="9389c-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="9389c-150">Un rectángulo de píxeles que comienza con las coordenadas de la ventana *x* *e y,* y con el *ancho* y el *alto* de las dimensiones reemplaza la parte de la matriz de textura con los índices *xoffset* a *xoffset* + (*width* -1), con los índices *YOFFSET* a *YOFFSET* + (*width* -1) en el nivel de mipmap especificado por *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="9389c-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="9389c-151">El rectángulo de destino de la matriz de textura no puede incluir ningún textura fuera de la matriz de textura especificada originalmente.</span><span class="sxs-lookup"><span data-stu-id="9389c-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="9389c-152">La función **glCopyTexSubImage2D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md), salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="9389c-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="9389c-153">El orden de los píxeles se determina con las coordenadas *x* inferiores correspondientes a las coordenadas de textura inferiores.</span><span class="sxs-lookup"><span data-stu-id="9389c-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="9389c-154">Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="9389c-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="9389c-155">Si alguno de los píxeles del rectángulo especificado del fotogramas actual está fuera de la ventana de lectura asociada al contexto de representación actual, los valores obtenidos para esos píxeles serán indefinidos.</span><span class="sxs-lookup"><span data-stu-id="9389c-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="9389c-156">No se realiza ningún cambio en el parámetro *internalFormat*, *width*, *height* o *Border* de la matriz de textura especificada o en textura valores fuera de la subimagen de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="9389c-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="9389c-157">No puede incluir llamadas a **glCopyTexSubImage2D** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="9389c-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="9389c-158">La función **glCopyTexSubImage2D** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9389c-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="9389c-159">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="9389c-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="9389c-160">Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la forma en que afectan al modo en que se dibujan los píxeles mediante [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="9389c-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="9389c-161">Las siguientes funciones recuperan información relacionada con **glCopyTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="9389c-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="9389c-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="9389c-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="9389c-163">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="9389c-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="9389c-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9389c-164">Requirements</span></span>



| <span data-ttu-id="9389c-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="9389c-165">Requirement</span></span> | <span data-ttu-id="9389c-166">Value</span><span class="sxs-lookup"><span data-stu-id="9389c-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9389c-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9389c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9389c-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9389c-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9389c-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9389c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9389c-170">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9389c-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9389c-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9389c-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="9389c-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9389c-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9389c-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="9389c-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9389c-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9389c-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9389c-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9389c-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9389c-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="9389c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9389c-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9389c-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9389c-179">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="9389c-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="9389c-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="9389c-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="9389c-181">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="9389c-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="9389c-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9389c-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9389c-183">**glFog**</span><span class="sxs-lookup"><span data-stu-id="9389c-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="9389c-184">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="9389c-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="9389c-185">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="9389c-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="9389c-186">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="9389c-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="9389c-187">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="9389c-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="9389c-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="9389c-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="9389c-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="9389c-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="9389c-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="9389c-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





