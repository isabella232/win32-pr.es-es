---
title: función glRasterPos4s (GL. h)
description: Especifica la posición de la trama para las operaciones de píxel. | función glRasterPos4s (GL. h)
ms.assetid: 60e6ced4-a542-4189-a3da-eed36f81cafb
keywords:
- glRasterPos4s (función) OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e9cbef5696abfb5e526881a88bda61c22e53c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670127"
---
# <a name="glrasterpos4s-function"></a><span data-ttu-id="44a82-105">glRasterPos4s función)</span><span class="sxs-lookup"><span data-stu-id="44a82-105">glRasterPos4s function</span></span>

<span data-ttu-id="44a82-106">Especifica la posición de la trama para las operaciones de píxel.</span><span class="sxs-lookup"><span data-stu-id="44a82-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a82-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44a82-107">Syntax</span></span>


```C++
void WINAPI glRasterPos4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
);
```



## <a name="parameters"></a><span data-ttu-id="44a82-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44a82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a82-109">*x*</span><span class="sxs-lookup"><span data-stu-id="44a82-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="44a82-110">Especifica la coordenada x de la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="44a82-110">Specifies the x-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="44a82-111">*y*</span><span class="sxs-lookup"><span data-stu-id="44a82-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="44a82-112">Especifica la coordenada y de la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="44a82-112">Specifies the y-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="44a82-113">*z*</span><span class="sxs-lookup"><span data-stu-id="44a82-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="44a82-114">Especifica la coordenada z de la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="44a82-114">Specifies the z-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="44a82-115">*w*</span><span class="sxs-lookup"><span data-stu-id="44a82-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="44a82-116">Coordenada w de la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="44a82-116">The w-coordinate for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a82-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44a82-117">Return value</span></span>

<span data-ttu-id="44a82-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="44a82-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44a82-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44a82-119">Remarks</span></span>

<span data-ttu-id="44a82-120">OpenGL mantiene una posición 3D en las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="44a82-120">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="44a82-121">Esta posición, denominada posición de la trama, se mantiene con una precisión de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="44a82-121">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="44a82-122">Se utiliza para colocar las operaciones de escritura de píxeles y de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="44a82-122">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="44a82-123">Vea [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)y [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="44a82-123">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="44a82-124">La posición de rasterización actual consta de tres coordenadas de ventana (*x, y, z*), un valor de coordenada de clip *w* , una distancia de coordenadas ocular, un bit válido y las coordenadas de textura y datos de color asociados.</span><span class="sxs-lookup"><span data-stu-id="44a82-124">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="44a82-125">La coordenada *w* es una coordenada de clip, porque *w* no se proyecta en coordenadas de ventana.</span><span class="sxs-lookup"><span data-stu-id="44a82-125">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="44a82-126">La función [glRasterPos4](glrasterpos-functions.md) especifica las coordenadas de objeto *x, y, z* y *w* explícitamente.</span><span class="sxs-lookup"><span data-stu-id="44a82-126">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="44a82-127">La función glRasterPos3 especifica las coordenadas de objeto *x,* y y *z* explícitamente, mientras que *w* se establece implícitamente en una.</span><span class="sxs-lookup"><span data-stu-id="44a82-127">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="44a82-128">La función glRasterPos2 usa los valores de argumento para *x* e *y mientras establece* implícitamente *z* y *w* en cero y en uno.</span><span class="sxs-lookup"><span data-stu-id="44a82-128">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="44a82-129">Las coordenadas de objeto presentadas por [glRasterPos](glrasterpos-functions.md) se tratan igual que las de un comando [glVertex](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="44a82-129">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="44a82-130">Los transforman las matrices de proyección y MODELVIEW actuales y se pasan a la fase de recorte.</span><span class="sxs-lookup"><span data-stu-id="44a82-130">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="44a82-131">Si no se selecciona el vértice, se proyecta y se escala a las coordenadas de la ventana, que se convierten en la nueva posición de la trama actual y \_ \_ \_ \_ se establece la marca válida de la posición de rasterización actual de GL.</span><span class="sxs-lookup"><span data-stu-id="44a82-131">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="44a82-132">Si se selecciona el vértice, se borra el bit válido y la posición de la trama actual y las coordenadas de textura y color asociadas no están definidas.</span><span class="sxs-lookup"><span data-stu-id="44a82-132">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="44a82-133">La posición de la trama actual también incluye algunos datos de color y coordenadas de textura asociados.</span><span class="sxs-lookup"><span data-stu-id="44a82-133">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="44a82-134">Si está habilitada la iluminación, \_ \_ el color de rasterizado actual \_ de GL, en el modo RGBA o el \_ Índice de \_ rasterización actual de GL \_ , en modo de índice de color, se establece en el color producido por el cálculo de iluminación (vea [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)y [**glShadeModel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="44a82-134">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="44a82-135">Si la iluminación está deshabilitada, se usa el color actual (en modo RGBA, la variable de estado GL \_ Current \_ color) o el índice de color (en modo de índice de color, variable de estado, \_ índice actual de contabilidad \_ ) para actualizar el color de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="44a82-135">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="44a82-136">Del mismo modo, las \_ \_ coordenadas de textura de rasterizado actual \_ de GL \_ se actualizan como una función de las \_ coordenadas de textura actual de GL \_ \_ , en función de la matriz de textura y las funciones de generación de textura (vea [glTexGen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="44a82-136">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="44a82-137">Por último, la distancia desde el origen del sistema de coordenadas del ojo hasta el vértice, tal y como se transforma solo en la matriz MODELVIEW, reemplaza a la distancia de la \_ trama actual de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="44a82-137">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="44a82-138">Inicialmente, la posición de la trama actual es (0, 0, 0, 1), la distancia de la trama actual es 0, se establece el bit válido, el color RGBA asociado es (1, 1, 1, 1), el índice de color asociado es 1 y las coordenadas de textura asociadas son (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="44a82-138">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="44a82-139">En el modo RGBA, \_ el índice de rasterizado actual de GL siempre \_ \_ es 1; en el modo de índice de color, el color RGBA de trama actual siempre mantiene su valor inicial.</span><span class="sxs-lookup"><span data-stu-id="44a82-139">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="44a82-140">[GlRasterPos](glrasterpos-functions.md) y [**glBitmap**](glbitmap.md)modifican la posición de la trama.</span><span class="sxs-lookup"><span data-stu-id="44a82-140">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="44a82-141">Cuando las coordenadas de posición de trama no son válidas, los comandos de dibujo que se basan en la posición de la trama se omiten (es decir, no producen cambios en el estado de OpenGL).</span><span class="sxs-lookup"><span data-stu-id="44a82-141">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="44a82-142">Las siguientes funciones recuperan información relacionada con [glRasterPos](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="44a82-142">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="44a82-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="44a82-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="44a82-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido</span><span class="sxs-lookup"><span data-stu-id="44a82-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="44a82-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ distancia de trama actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="44a82-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="44a82-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ color de RASTERIZAdo actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="44a82-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="44a82-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ Índice de trama actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="44a82-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="44a82-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ \_ textura de RASTERIZAdo actual \_ de GL \_</span><span class="sxs-lookup"><span data-stu-id="44a82-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="44a82-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a82-149">Requirements</span></span>



| <span data-ttu-id="44a82-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a82-150">Requirement</span></span> | <span data-ttu-id="44a82-151">Value</span><span class="sxs-lookup"><span data-stu-id="44a82-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44a82-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44a82-152">Minimum supported client</span></span><br/> | <span data-ttu-id="44a82-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="44a82-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="44a82-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44a82-154">Minimum supported server</span></span><br/> | <span data-ttu-id="44a82-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44a82-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44a82-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44a82-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a82-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="44a82-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="44a82-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44a82-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="44a82-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44a82-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="44a82-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44a82-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a82-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44a82-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a82-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="44a82-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a82-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="44a82-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="44a82-164">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="44a82-164">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="44a82-165">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="44a82-165">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="44a82-166">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="44a82-166">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="44a82-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="44a82-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="44a82-168">glLight</span><span class="sxs-lookup"><span data-stu-id="44a82-168">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="44a82-169">glLightModel</span><span class="sxs-lookup"><span data-stu-id="44a82-169">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="44a82-170">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="44a82-170">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="44a82-171">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="44a82-171">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="44a82-172">glTexGen</span><span class="sxs-lookup"><span data-stu-id="44a82-172">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="44a82-173">glVertex</span><span class="sxs-lookup"><span data-stu-id="44a82-173">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





