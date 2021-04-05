---
title: función glCopyTexSubImage1D (GL. h)
description: La función glCopyTexSubImage1D copia una subimagen de una imagen de textura de una dimensión de fotogramas.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D (función) OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996624"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="88df6-104">glCopyTexSubImage1D función)</span><span class="sxs-lookup"><span data-stu-id="88df6-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="88df6-105">La función **glCopyTexSubImage1D** copia una subimagen de una imagen de textura de una dimensión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="88df6-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="88df6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88df6-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="88df6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88df6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88df6-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="88df6-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="88df6-109">Destino al que se cambiarán los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="88df6-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="88df6-110">Debe tener el valor de GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="88df6-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="88df6-111">*level*</span><span class="sxs-lookup"><span data-stu-id="88df6-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="88df6-112">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="88df6-112">The level-of-detail number.</span></span> <span data-ttu-id="88df6-113">El nivel 0 es la imagen base.</span><span class="sxs-lookup"><span data-stu-id="88df6-113">Level 0 is the base image.</span></span> <span data-ttu-id="88df6-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="88df6-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="88df6-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="88df6-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="88df6-116">Desplazamiento textura dentro de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="88df6-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="88df6-117">*x*</span><span class="sxs-lookup"><span data-stu-id="88df6-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="88df6-118">Coordenada x del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="88df6-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="88df6-119">*y*</span><span class="sxs-lookup"><span data-stu-id="88df6-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="88df6-120">Coordenada y del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="88df6-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="88df6-121">*width*</span><span class="sxs-lookup"><span data-stu-id="88df6-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="88df6-122">Ancho de la subimagen de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="88df6-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="88df6-123">Especificar una subimagen de textura con un ancho de cero no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="88df6-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88df6-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88df6-124">Return value</span></span>

<span data-ttu-id="88df6-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="88df6-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88df6-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="88df6-126">Error codes</span></span>

<span data-ttu-id="88df6-127">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="88df6-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="88df6-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="88df6-128">Name</span></span>                                                                                                  | <span data-ttu-id="88df6-129">Significado</span><span class="sxs-lookup"><span data-stu-id="88df6-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88df6-130"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="88df6-131">el *destino* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="88df6-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="88df6-132"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="88df6-133">el *nivel* era menor que cero o el *nivel* es mayor que el *registro* 2 (*Max*), donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="88df6-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="88df6-134"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="88df6-135">*xoffset* era menor que *Border* o (el  +  *ancho* de xoffset) era mayor que (*w*  +  *Border*), donde *w* es el \_ ancho y el borde de la textura GL \_ es  \_ Border Texture \_ Border.</span><span class="sxs-lookup"><span data-stu-id="88df6-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="88df6-136">Tenga en cuenta que *w* incluye dos veces el ancho del *borde* .</span><span class="sxs-lookup"><span data-stu-id="88df6-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="88df6-137"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="88df6-138">el *ancho* era menor *que Border* o *y* era menor que *Border*, donde *Border* es el ancho del borde de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="88df6-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="88df6-139"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="88df6-140">Una operación [**glTexImage1D**](glteximage1d.md) anterior no definió la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="88df6-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="88df6-141"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="88df6-142">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="88df6-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="88df6-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88df6-143">Remarks</span></span>

<span data-ttu-id="88df6-144">La función **glCopyTexSubImage1D** reemplaza una parte de una imagen de textura de una dimensión mediante píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexSubImage1D**](gltexsubimage1d.md).</span><span class="sxs-lookup"><span data-stu-id="88df6-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="88df6-145">Una fila de píxeles que comienza con las coordenadas de la ventana especificadas por *x* *e y y con* el *ancho* de longitud reemplaza a la parte de la matriz de textura con los índices *xoffset* a *xoffset* + (*width* -1).</span><span class="sxs-lookup"><span data-stu-id="88df6-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="88df6-146">El destino de la matriz de textura no puede incluir ningún textura fuera de la matriz de textura especificada originalmente.</span><span class="sxs-lookup"><span data-stu-id="88df6-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="88df6-147">La función **glCopyTexSubImage1D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md) , salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="88df6-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="88df6-148">El orden de los píxeles se determina con las coordenadas *x* inferiores correspondientes a las coordenadas de textura inferiores.</span><span class="sxs-lookup"><span data-stu-id="88df6-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="88df6-149">Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="88df6-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="88df6-150">No se realiza ningún cambio en el parámetro *internalFormat*, *width* o *Border* de la matriz de textura especificada o en textura valores fuera de la subimagen de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="88df6-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="88df6-151">No puede incluir llamadas a **glCopyTexSubImage1D** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="88df6-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="88df6-152">La función **glCopyTexSubImage1D** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="88df6-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="88df6-153">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="88df6-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="88df6-154">Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la forma en que afectan al modo en que se dibujan los píxeles mediante [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="88df6-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="88df6-155">Las siguientes funciones recuperan información relacionada con **glCopyTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="88df6-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="88df6-156">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="88df6-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="88df6-157">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="88df6-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="88df6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88df6-158">Requirements</span></span>



| <span data-ttu-id="88df6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="88df6-159">Requirement</span></span> | <span data-ttu-id="88df6-160">Value</span><span class="sxs-lookup"><span data-stu-id="88df6-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88df6-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88df6-161">Minimum supported client</span></span><br/> | <span data-ttu-id="88df6-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="88df6-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="88df6-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88df6-163">Minimum supported server</span></span><br/> | <span data-ttu-id="88df6-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88df6-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88df6-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88df6-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="88df6-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="88df6-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88df6-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="88df6-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="88df6-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88df6-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88df6-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88df6-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88df6-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="88df6-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88df6-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="88df6-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="88df6-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="88df6-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="88df6-174">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="88df6-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="88df6-175">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="88df6-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="88df6-176">**glFog**</span><span class="sxs-lookup"><span data-stu-id="88df6-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="88df6-177">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="88df6-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="88df6-178">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="88df6-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="88df6-179">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="88df6-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="88df6-180">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="88df6-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="88df6-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="88df6-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="88df6-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="88df6-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="88df6-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="88df6-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="88df6-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="88df6-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="88df6-185">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="88df6-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





