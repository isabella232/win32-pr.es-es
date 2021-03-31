---
title: función gluTessProperty (GLU. h)
description: La función gluTessProperty establece la propiedad de un objeto de teselación.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- gluTessProperty (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151025"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="aac47-104">gluTessProperty función)</span><span class="sxs-lookup"><span data-stu-id="aac47-104">gluTessProperty function</span></span>

<span data-ttu-id="aac47-105">La función **gluTessProperty** establece la propiedad de un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="aac47-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac47-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aac47-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="aac47-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aac47-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac47-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="aac47-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="aac47-109">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="aac47-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="aac47-110">*cuales*</span><span class="sxs-lookup"><span data-stu-id="aac47-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="aac47-111">Valor de la propiedad que se establecerá.</span><span class="sxs-lookup"><span data-stu-id="aac47-111">The property value to set.</span></span> <span data-ttu-id="aac47-112">Los valores siguientes son válidos: \_ Glu \_ Tess \_ , Glu \_ Tess \_ BOUNDARY \_ y Glu \_ Tess \_ Tolerance.</span><span class="sxs-lookup"><span data-stu-id="aac47-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="aac47-113">Value</span><span class="sxs-lookup"><span data-stu-id="aac47-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="aac47-114">Significado</span><span class="sxs-lookup"><span data-stu-id="aac47-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="aac47-115"><dt>**GLU \_ \_ regla de bobinado de Tess \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aac47-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="aac47-116">Determina qué partes del polígono se encuentran en el interior.</span><span class="sxs-lookup"><span data-stu-id="aac47-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="aac47-117">El parámetro de valor se puede establecer en uno de los siguientes: GLU \_ Tess \_ bobinado \_ impar, Glu \_ Tess \_ bobinado \_ unzero, Glu \_ Tess \_ devanado \_ Positive, Glu \_ Tess \_ bobinado \_ negative o Glu \_ Tess \_ bobinado \_ ABS \_ GEQ \_ Two.</span><span class="sxs-lookup"><span data-stu-id="aac47-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="aac47-118">Para entender cómo funciona la regla de bobinado, considere primero que los contornos de entrada particionan el plano en regiones.</span><span class="sxs-lookup"><span data-stu-id="aac47-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="aac47-119">La regla de bobinado determina cuál de estas regiones se encuentra dentro del polígono.</span><span class="sxs-lookup"><span data-stu-id="aac47-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="aac47-120">En el caso de un solo contorno C, el número de bobinado de un punto x es simplemente el número de revoluciones con signo que hacemos alrededor de x a medida que nos desplazamos una vez alrededor de C (donde el sentido contrario a las agujas del reloj es positivo).</span><span class="sxs-lookup"><span data-stu-id="aac47-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="aac47-121">Cuando hay varios contornos, se suman los números de bobinado individuales.</span><span class="sxs-lookup"><span data-stu-id="aac47-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="aac47-122">Este procedimiento asocia un valor entero con signo a cada punto x del plano.</span><span class="sxs-lookup"><span data-stu-id="aac47-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="aac47-123">Tenga en cuenta que el número de bobinado es el mismo para todos los puntos de una sola región.</span><span class="sxs-lookup"><span data-stu-id="aac47-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="aac47-124">La regla de bobinado clasifica una región como "dentro" Si su número de bobinado pertenece a la categoría elegida (impar, distinto de cero, positivo, negativo o valor absoluto de al menos dos).</span><span class="sxs-lookup"><span data-stu-id="aac47-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="aac47-125">La GLU anterior del teselador (anterior a GLU 1,2) usaba la regla "impar".</span><span class="sxs-lookup"><span data-stu-id="aac47-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="aac47-126">La regla "NonZero" (GLU \_ Tess \_ sinuoso \_ noncero) es otra forma habitual de definir el interior.</span><span class="sxs-lookup"><span data-stu-id="aac47-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="aac47-127">Las otras tres reglas (GLU \_ Tess \_ devanado \_ positivo, Glu \_ Tess \_ bobinado \_ negativo, Glu \_ Tess \_ bobinado \_ ABS \_ GEQ \_ dos) son útiles para las operaciones de Polygon CSG.</span><span class="sxs-lookup"><span data-stu-id="aac47-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="aac47-128"><dt>**\_ \_ solo límites de Tess de Glu \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aac47-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="aac47-129">Especifica un valor booleano (establecer valor en GL \_ true o GL \_ false).</span><span class="sxs-lookup"><span data-stu-id="aac47-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="aac47-130">Al establecer Value en GL \_ true, se devuelve un conjunto de contornos cerrados que separan el interior y el exterior del polígono en lugar de una teselación.</span><span class="sxs-lookup"><span data-stu-id="aac47-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="aac47-131">Los contornos exteriores se orientan en sentido contrario a las agujas del reloj con respecto al normal; los contornos interiores están orientados a la derecha.</span><span class="sxs-lookup"><span data-stu-id="aac47-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="aac47-132">Las \_ \_ \_ devoluciones de llamada de datos Begin y GLU Tess de Glu Tess \_ \_ usan el tipo \_ \_ de bucle de línea de libro de contabilidad para cada perfil.</span><span class="sxs-lookup"><span data-stu-id="aac47-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="aac47-133"><dt>**\_tolerancia Tess \_ Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="aac47-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="aac47-134">Especifica una tolerancia para la combinación de características para reducir el tamaño de la salida.</span><span class="sxs-lookup"><span data-stu-id="aac47-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="aac47-135">Por ejemplo, dos vértices que son muy cercanos entre sí se pueden reemplazar por un solo vértice.</span><span class="sxs-lookup"><span data-stu-id="aac47-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="aac47-136">La tolerancia se multiplica por la magnitud de la coordenada más grande de cualquier vértice de entrada; Especifica la distancia máxima que cualquier característica puede moverse como resultado de una sola operación de combinación.</span><span class="sxs-lookup"><span data-stu-id="aac47-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="aac47-137">Si una sola característica participa en varias operaciones de combinación, la distancia total movida puede ser mayor.</span><span class="sxs-lookup"><span data-stu-id="aac47-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="aac47-138">La combinación de características es totalmente opcional; la tolerancia es solo una sugerencia.</span><span class="sxs-lookup"><span data-stu-id="aac47-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="aac47-139">La implementación es gratuita para la fusión mediante combinación en algunos casos, no en otras o para no combinar nunca características.</span><span class="sxs-lookup"><span data-stu-id="aac47-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="aac47-140">La tolerancia predeterminada es cero.</span><span class="sxs-lookup"><span data-stu-id="aac47-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="aac47-141">La implementación actual combina los vértices solo si son exactamente coincidentes, independientemente de la tolerancia actual.</span><span class="sxs-lookup"><span data-stu-id="aac47-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="aac47-142">Un vértice se une a un borde solo si la implementación no puede distinguir en qué lado del borde reside el vértice.</span><span class="sxs-lookup"><span data-stu-id="aac47-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="aac47-143">Dos bordes se combinan solo cuando ambos extremos son idénticos.</span><span class="sxs-lookup"><span data-stu-id="aac47-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="aac47-144">*value*</span><span class="sxs-lookup"><span data-stu-id="aac47-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="aac47-145">Valor de la propiedad indicada.</span><span class="sxs-lookup"><span data-stu-id="aac47-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac47-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aac47-146">Return value</span></span>

<span data-ttu-id="aac47-147">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aac47-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac47-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aac47-148">Remarks</span></span>

<span data-ttu-id="aac47-149">La función **gluTessProperty** controla las propiedades almacenadas en un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="aac47-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="aac47-150">Estas propiedades afectan a la manera en que se interpretan y representan los polígonos.</span><span class="sxs-lookup"><span data-stu-id="aac47-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac47-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aac47-151">Requirements</span></span>



| <span data-ttu-id="aac47-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="aac47-152">Requirement</span></span> | <span data-ttu-id="aac47-153">Value</span><span class="sxs-lookup"><span data-stu-id="aac47-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aac47-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aac47-154">Minimum supported client</span></span><br/> | <span data-ttu-id="aac47-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aac47-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aac47-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aac47-156">Minimum supported server</span></span><br/> | <span data-ttu-id="aac47-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aac47-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aac47-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aac47-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac47-159"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="aac47-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="aac47-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aac47-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="aac47-161"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aac47-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aac47-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aac47-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aac47-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aac47-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac47-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="aac47-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac47-165">**gluGetTessProperty**</span><span class="sxs-lookup"><span data-stu-id="aac47-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="aac47-166">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="aac47-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





