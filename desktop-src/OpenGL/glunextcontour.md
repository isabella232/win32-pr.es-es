---
title: función gluNextContour (GLU. h)
description: La función gluNextContour marca el principio de otro contorno.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour (función) OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422109"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="ed62f-104">gluNextContour función)</span><span class="sxs-lookup"><span data-stu-id="ed62f-104">gluNextContour function</span></span>

<span data-ttu-id="ed62f-105">\[La función **gluNextContour** está obsoleta y solo se proporciona por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ed62f-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="ed62f-106">La función **gluNextContour** se asigna a [**GluTessEndContour**](glutessendcontour.md) seguido de [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="ed62f-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="ed62f-107">La función **gluNextContour** marca el principio de otro contorno.</span><span class="sxs-lookup"><span data-stu-id="ed62f-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed62f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed62f-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="ed62f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed62f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed62f-110">*tess*</span><span class="sxs-lookup"><span data-stu-id="ed62f-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="ed62f-111">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="ed62f-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ed62f-112">*type*</span><span class="sxs-lookup"><span data-stu-id="ed62f-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="ed62f-113">Tipo del contorno que se va a definir.</span><span class="sxs-lookup"><span data-stu-id="ed62f-113">The type of the contour being defined.</span></span> <span data-ttu-id="ed62f-114">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="ed62f-114">The following values are valid.</span></span>



| <span data-ttu-id="ed62f-115">Value</span><span class="sxs-lookup"><span data-stu-id="ed62f-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="ed62f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ed62f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="ed62f-117"><dt>**GLU \_ exterior**</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="ed62f-118">Un contorno exterior define un límite exterior del polígono.</span><span class="sxs-lookup"><span data-stu-id="ed62f-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="ed62f-119"><dt>**\_interior Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="ed62f-120">Un contorno interior define un límite interior del polígono (por ejemplo, un hueco).</span><span class="sxs-lookup"><span data-stu-id="ed62f-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="ed62f-121"><dt>**GLU \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="ed62f-122">La biblioteca analiza un perfil desconocido para determinar si es interior o exterior.</span><span class="sxs-lookup"><span data-stu-id="ed62f-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="ed62f-123"><dt>**GLU \_ CCW, Glu \_ CW**</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="ed62f-124">Se considera que el primer \_ contorno Glu CCW o Glu \_ CW definido es exterior.</span><span class="sxs-lookup"><span data-stu-id="ed62f-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="ed62f-125">El resto de los contornos se consideran exteriores si están orientados en la misma dirección (en el sentido de las agujas del reloj o en el sentido contrario a las agujas del reloj) como el primer perfil y interior si no lo están.</span><span class="sxs-lookup"><span data-stu-id="ed62f-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="ed62f-126">Si un contorno es de tipo GLU \_ CCW o Glu CW, todos los contornos \_ deben ser del mismo tipo (si no lo son, todos los contornos de Glu \_ CCW y Glu \_ CW se cambiarán a Glu \_ Unknown).</span><span class="sxs-lookup"><span data-stu-id="ed62f-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="ed62f-127">Tenga en cuenta que no hay ninguna diferencia real entre los \_ tipos de contorno Glu CCW y Glu \_ CW.</span><span class="sxs-lookup"><span data-stu-id="ed62f-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed62f-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed62f-128">Return value</span></span>

<span data-ttu-id="ed62f-129">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ed62f-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed62f-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed62f-130">Remarks</span></span>

<span data-ttu-id="ed62f-131">Use la función **gluNextContour** para describir polígonos con varios contornos.</span><span class="sxs-lookup"><span data-stu-id="ed62f-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="ed62f-132">Después de describir el primer contorno a través de una serie de llamadas de [**gluTessVertex**](glutessvertex.md) , una llamada a **gluNextContour** indica que el contorno anterior está completo y que el siguiente perfil está a punto de comenzar.</span><span class="sxs-lookup"><span data-stu-id="ed62f-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="ed62f-133">Realice otra serie de llamadas de **gluTessVertex** para describir el nuevo contorno.</span><span class="sxs-lookup"><span data-stu-id="ed62f-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="ed62f-134">Repita este proceso hasta que se hayan descrito todos los contornos.</span><span class="sxs-lookup"><span data-stu-id="ed62f-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="ed62f-135">El parámetro de *tipo* define el tipo de perfil que sigue.</span><span class="sxs-lookup"><span data-stu-id="ed62f-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="ed62f-136">Para definir el tipo del primer perfil, puede llamar a **gluNextContour** antes de describir el primer contorno.</span><span class="sxs-lookup"><span data-stu-id="ed62f-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="ed62f-137">Si no llama a **gluNextContour** antes del primer perfil, el primer contorno está marcado como Glu \_ exterior.</span><span class="sxs-lookup"><span data-stu-id="ed62f-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="ed62f-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed62f-138">Examples</span></span>

<span data-ttu-id="ed62f-139">Puede describir un cuadrangular con un orificio triangular en él de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed62f-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="ed62f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed62f-140">Requirements</span></span>



| <span data-ttu-id="ed62f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed62f-141">Requirement</span></span> | <span data-ttu-id="ed62f-142">Value</span><span class="sxs-lookup"><span data-stu-id="ed62f-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed62f-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed62f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ed62f-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ed62f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ed62f-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed62f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ed62f-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed62f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ed62f-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed62f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed62f-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ed62f-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed62f-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed62f-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ed62f-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed62f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed62f-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed62f-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed62f-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed62f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed62f-154">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="ed62f-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="ed62f-155">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="ed62f-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="ed62f-156">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="ed62f-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="ed62f-157">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="ed62f-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="ed62f-158">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="ed62f-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="ed62f-159">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="ed62f-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





