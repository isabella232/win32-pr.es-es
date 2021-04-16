---
title: función glGetTexImage (GL. h)
description: La función glGetTexImage devuelve una imagen de textura.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666071"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="5047c-104">glGetTexImage función)</span><span class="sxs-lookup"><span data-stu-id="5047c-104">glGetTexImage function</span></span>

<span data-ttu-id="5047c-105">La función **glGetTexImage** devuelve una imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="5047c-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="5047c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5047c-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="5047c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5047c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5047c-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="5047c-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5047c-109">Especifica la textura que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="5047c-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="5047c-110">Se aceptan las texturas GL \_ \_ 1D y GL Texture \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5047c-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5047c-111">*level*</span><span class="sxs-lookup"><span data-stu-id="5047c-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="5047c-112">El número de nivel de detalle de la imagen deseada.</span><span class="sxs-lookup"><span data-stu-id="5047c-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="5047c-113">El nivel 0 es el nivel de la imagen base.</span><span class="sxs-lookup"><span data-stu-id="5047c-113">Level 0 is the base image level.</span></span> <span data-ttu-id="5047c-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="5047c-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="5047c-115">*format*</span><span class="sxs-lookup"><span data-stu-id="5047c-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="5047c-116">Formato de píxel para los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="5047c-116">A pixel format for the returned data.</span></span> <span data-ttu-id="5047c-117">Los formatos admitidos son GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ luminancia, GL \_ BGR \_ ext, GL \_ BGRA \_ EXT y luminancia de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5047c-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="5047c-118">*type*</span><span class="sxs-lookup"><span data-stu-id="5047c-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="5047c-119">Un tipo de píxel para los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="5047c-119">A pixel type for the returned data.</span></span> <span data-ttu-id="5047c-120">Los tipos admitidos son el \_ byte sin signo de GL \_ , GL \_ byte, GL \_ sin signo \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int y GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="5047c-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="5047c-121">*píxeles*</span><span class="sxs-lookup"><span data-stu-id="5047c-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="5047c-122">Devuelve la imagen de la textura.</span><span class="sxs-lookup"><span data-stu-id="5047c-122">Returns the texture image.</span></span> <span data-ttu-id="5047c-123">Debe ser un puntero a una matriz del tipo especificado por el *tipo*.</span><span class="sxs-lookup"><span data-stu-id="5047c-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5047c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5047c-124">Return value</span></span>

<span data-ttu-id="5047c-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5047c-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5047c-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5047c-126">Error codes</span></span>

<span data-ttu-id="5047c-127">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="5047c-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5047c-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="5047c-128">Name</span></span>                                                                                                  | <span data-ttu-id="5047c-129">Significado</span><span class="sxs-lookup"><span data-stu-id="5047c-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5047c-130"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5047c-131">*destino*, *formato* o *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="5047c-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="5047c-132"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5047c-133">el *nivel* es menor que cero o mayor que el *registro* 2 (*Max*), donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5047c-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="5047c-134"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5047c-135">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="5047c-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5047c-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5047c-136">Remarks</span></span>

<span data-ttu-id="5047c-137">La función **glGetTexImage** devuelve una imagen de textura en *píxeles*.</span><span class="sxs-lookup"><span data-stu-id="5047c-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="5047c-138">El parámetro de *destino* especifica si la imagen de textura deseada es una especificada por [**glTexImage1D**](glteximage1d.md)**(** GL \_ Texture \_ 1D **)** o por [**glTexImage2D**](glteximage2d.md)**(** GL \_ Texture \_ 2D **)**.</span><span class="sxs-lookup"><span data-stu-id="5047c-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="5047c-139">El parámetro *LEVEL* especifica el número de nivel de detalle de la imagen deseada.</span><span class="sxs-lookup"><span data-stu-id="5047c-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="5047c-140">Los parámetros de *tipo* y *formato* especifican el formato y el tipo de la matriz de imágenes deseada.</span><span class="sxs-lookup"><span data-stu-id="5047c-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="5047c-141">Para obtener una descripción de los valores aceptables para los parámetros de *formato* y *tipo* , respectivamente, vea **glTexImage1D** y [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="5047c-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="5047c-142">La operación de **glGetTexImage** se entiende mejor teniendo en cuenta que la imagen de textura interna de cuatro componentes seleccionada es un búfer de color RGBA el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="5047c-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="5047c-143">La semántica de **glGetTexImage** es idéntica a la de [**glReadPixels**](glreadpixels.md) a la que se llama con el mismo *formato* y *tipo*. con *x* e y establecido en cero, el *ancho* *se establece en* el ancho de la imagen de textura (incluido el borde si se especificó) y el *alto* se establece en uno para las imágenes 1D, o en el alto de la imagen de textura (incluido el borde, si se ha especificado) para las imágenes 2D.</span><span class="sxs-lookup"><span data-stu-id="5047c-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="5047c-144">Dado que la imagen de textura interna es una imagen RGBA, no se aceptan los formatos de píxel \_ \_ Índice de color de contabilidad, índice de estarcido de GL \_ \_ y componente de profundidad de libro de contabilidad \_ \_ , y no se acepta el mapa de bits de contabilidad de tipo píxel \_ .</span><span class="sxs-lookup"><span data-stu-id="5047c-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="5047c-145">Si la imagen de textura seleccionada no contiene cuatro componentes, se aplican las siguientes asignaciones.</span><span class="sxs-lookup"><span data-stu-id="5047c-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="5047c-146">Las texturas de un solo componente se tratan como búferes RGBA con el rojo establecido en el valor de un solo componente, y el verde, el azul y el alfa se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="5047c-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="5047c-147">Las texturas de dos componentes se tratan como búferes RGBA, con el rojo establecido en el valor de componente cero, alfa establecido en el valor del componente uno, y en verde y azul establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="5047c-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="5047c-148">Por último, las texturas de tres componentes se tratan como búferes RGBA con el valor rojo establecido en componente cero, verde establecido en componente uno, azul establecido en componente dos y alfa establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="5047c-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="5047c-149">Para determinar el tamaño necesario de los *píxeles*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) para determinar las dimensiones de la imagen de textura interna y, a continuación, escale el número necesario de píxeles según el almacenamiento necesario para cada píxel, en función del *formato* y el *tipo*.</span><span class="sxs-lookup"><span data-stu-id="5047c-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="5047c-150">Asegúrese de tener en cuenta los parámetros de almacenamiento de píxeles, especialmente la \_ alineación del paquete GL \_ .</span><span class="sxs-lookup"><span data-stu-id="5047c-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="5047c-151">Si se genera un error, no se realiza ningún cambio en el contenido de los *píxeles*.</span><span class="sxs-lookup"><span data-stu-id="5047c-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="5047c-152">Las siguientes funciones recuperan información relacionada con **glGetTexImage**:</span><span class="sxs-lookup"><span data-stu-id="5047c-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="5047c-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ alineación del paquete GL \_ y otros</span><span class="sxs-lookup"><span data-stu-id="5047c-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="5047c-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) con el argumento \_ ancho de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="5047c-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="5047c-155">**glGetTexLevelParameter** con el argumento \_ alto de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="5047c-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="5047c-156">**glGetTexLevelParameter** con el argumento \_ borde de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="5047c-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="5047c-157">**glGetTexLevelParameter** con \_ los componentes de textura GL de argument \_</span><span class="sxs-lookup"><span data-stu-id="5047c-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="5047c-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5047c-158">Requirements</span></span>



| <span data-ttu-id="5047c-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5047c-159">Requirement</span></span> | <span data-ttu-id="5047c-160">Value</span><span class="sxs-lookup"><span data-stu-id="5047c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5047c-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5047c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5047c-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5047c-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5047c-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5047c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5047c-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5047c-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5047c-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5047c-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="5047c-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5047c-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5047c-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="5047c-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5047c-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5047c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5047c-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5047c-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="5047c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5047c-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5047c-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5047c-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="5047c-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="5047c-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5047c-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5047c-175">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="5047c-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="5047c-176">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="5047c-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="5047c-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="5047c-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="5047c-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="5047c-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





