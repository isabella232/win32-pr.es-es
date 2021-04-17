---
title: función glRasterPos4dv (GL. h)
description: Especifica la posición de la trama para las operaciones de píxel. | función glRasterPos4dv (GL. h)
ms.assetid: d3f0ea80-6753-4c9d-a498-9166f6207692
keywords:
- glRasterPos4dv (función) OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2762cbc0dc6a1258aa194d320e214b49eb83cc8d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689728"
---
# <a name="glrasterpos4dv-function"></a><span data-ttu-id="1ddee-105">glRasterPos4dv función)</span><span class="sxs-lookup"><span data-stu-id="1ddee-105">glRasterPos4dv function</span></span>

<span data-ttu-id="1ddee-106">Especifica la posición de la trama para las operaciones de píxel.</span><span class="sxs-lookup"><span data-stu-id="1ddee-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ddee-107">Syntax</span></span>


```C++
void WINAPI glRasterPos4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="1ddee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ddee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ddee-109">*v*</span><span class="sxs-lookup"><span data-stu-id="1ddee-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="1ddee-110">Puntero a una matriz de cuatro elementos, que especifica las coordenadas x, y, z y w para la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="1ddee-110">A pointer to an array of four elements, specifying x, y, z, and w coordinates for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ddee-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ddee-111">Return value</span></span>

<span data-ttu-id="1ddee-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ddee-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ddee-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ddee-113">Remarks</span></span>

<span data-ttu-id="1ddee-114">OpenGL mantiene una posición 3D en las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ddee-114">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="1ddee-115">Esta posición, denominada posición de la trama, se mantiene con una precisión de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="1ddee-115">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="1ddee-116">Se utiliza para colocar las operaciones de escritura de píxeles y de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="1ddee-116">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="1ddee-117">Vea [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)y [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="1ddee-117">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="1ddee-118">La posición de rasterización actual consta de tres coordenadas de ventana (*x, y, z*), un valor de coordenada de clip *w* , una distancia de coordenadas ocular, un bit válido y las coordenadas de textura y datos de color asociados.</span><span class="sxs-lookup"><span data-stu-id="1ddee-118">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="1ddee-119">La coordenada *w* es una coordenada de clip, porque *w* no se proyecta en coordenadas de ventana.</span><span class="sxs-lookup"><span data-stu-id="1ddee-119">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="1ddee-120">La función [glRasterPos4](glrasterpos-functions.md) especifica las coordenadas de objeto *x, y, z* y *w* explícitamente.</span><span class="sxs-lookup"><span data-stu-id="1ddee-120">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="1ddee-121">La función glRasterPos3 especifica las coordenadas de objeto *x,* y y *z* explícitamente, mientras que *w* se establece implícitamente en una.</span><span class="sxs-lookup"><span data-stu-id="1ddee-121">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="1ddee-122">La función glRasterPos2 usa los valores de argumento para *x* e *y mientras establece* implícitamente *z* y *w* en cero y en uno.</span><span class="sxs-lookup"><span data-stu-id="1ddee-122">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="1ddee-123">Las coordenadas de objeto presentadas por [glRasterPos](glrasterpos-functions.md) se tratan igual que las de un comando [glVertex](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="1ddee-123">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="1ddee-124">Los transforman las matrices de proyección y MODELVIEW actuales y se pasan a la fase de recorte.</span><span class="sxs-lookup"><span data-stu-id="1ddee-124">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="1ddee-125">Si no se selecciona el vértice, se proyecta y se escala a las coordenadas de la ventana, que se convierten en la nueva posición de la trama actual y \_ \_ \_ \_ se establece la marca válida de la posición de rasterización actual de GL.</span><span class="sxs-lookup"><span data-stu-id="1ddee-125">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="1ddee-126">Si se selecciona el vértice, se borra el bit válido y la posición de la trama actual y las coordenadas de textura y color asociadas no están definidas.</span><span class="sxs-lookup"><span data-stu-id="1ddee-126">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="1ddee-127">La posición de la trama actual también incluye algunos datos de color y coordenadas de textura asociados.</span><span class="sxs-lookup"><span data-stu-id="1ddee-127">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="1ddee-128">Si está habilitada la iluminación, \_ \_ el color de rasterizado actual \_ de GL, en el modo RGBA o el \_ Índice de \_ rasterización actual de GL \_ , en modo de índice de color, se establece en el color producido por el cálculo de iluminación (vea [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)y [**glShadeModel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="1ddee-128">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="1ddee-129">Si la iluminación está deshabilitada, se usa el color actual (en modo RGBA, la variable de estado GL \_ Current \_ color) o el índice de color (en modo de índice de color, variable de estado, \_ índice actual de contabilidad \_ ) para actualizar el color de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="1ddee-129">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="1ddee-130">Del mismo modo, las \_ \_ coordenadas de textura de rasterizado actual \_ de GL \_ se actualizan como una función de las \_ coordenadas de textura actual de GL \_ \_ , en función de la matriz de textura y las funciones de generación de textura (vea [glTexGen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="1ddee-130">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="1ddee-131">Por último, la distancia desde el origen del sistema de coordenadas del ojo hasta el vértice, tal y como se transforma solo en la matriz MODELVIEW, reemplaza a la distancia de la \_ trama actual de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1ddee-131">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="1ddee-132">Inicialmente, la posición de la trama actual es (0, 0, 0, 1), la distancia de la trama actual es 0, se establece el bit válido, el color RGBA asociado es (1, 1, 1, 1), el índice de color asociado es 1 y las coordenadas de textura asociadas son (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1ddee-132">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="1ddee-133">En el modo RGBA, \_ el índice de rasterizado actual de GL siempre \_ \_ es 1; en el modo de índice de color, el color RGBA de trama actual siempre mantiene su valor inicial.</span><span class="sxs-lookup"><span data-stu-id="1ddee-133">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="1ddee-134">[GlRasterPos](glrasterpos-functions.md) y [**glBitmap**](glbitmap.md)modifican la posición de la trama.</span><span class="sxs-lookup"><span data-stu-id="1ddee-134">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="1ddee-135">Cuando las coordenadas de posición de trama no son válidas, los comandos de dibujo que se basan en la posición de la trama se omiten (es decir, no producen cambios en el estado de OpenGL).</span><span class="sxs-lookup"><span data-stu-id="1ddee-135">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="1ddee-136">Las siguientes funciones recuperan información relacionada con [glRasterPos](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="1ddee-136">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="1ddee-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="1ddee-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="1ddee-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido</span><span class="sxs-lookup"><span data-stu-id="1ddee-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="1ddee-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ distancia de trama actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="1ddee-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="1ddee-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ color de RASTERIZAdo actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="1ddee-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="1ddee-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ Índice de trama actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="1ddee-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="1ddee-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ \_ textura de RASTERIZAdo actual \_ de GL \_</span><span class="sxs-lookup"><span data-stu-id="1ddee-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="1ddee-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ddee-143">Requirements</span></span>



| <span data-ttu-id="1ddee-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ddee-144">Requirement</span></span> | <span data-ttu-id="1ddee-145">Value</span><span class="sxs-lookup"><span data-stu-id="1ddee-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddee-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ddee-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1ddee-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1ddee-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ddee-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ddee-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1ddee-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ddee-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ddee-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ddee-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ddee-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ddee-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1ddee-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ddee-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ddee-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ddee-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ddee-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ddee-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ddee-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ddee-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ddee-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ddee-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ddee-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1ddee-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1ddee-158">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="1ddee-158">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="1ddee-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="1ddee-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="1ddee-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="1ddee-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1ddee-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1ddee-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1ddee-162">glLight</span><span class="sxs-lookup"><span data-stu-id="1ddee-162">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="1ddee-163">glLightModel</span><span class="sxs-lookup"><span data-stu-id="1ddee-163">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="1ddee-164">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="1ddee-164">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="1ddee-165">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="1ddee-165">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1ddee-166">glTexGen</span><span class="sxs-lookup"><span data-stu-id="1ddee-166">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1ddee-167">glVertex</span><span class="sxs-lookup"><span data-stu-id="1ddee-167">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





