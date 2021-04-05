---
title: función glFrontFace (GL. h)
description: La función glFrontFace define polígonos orientados delante y detrás.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace (función) OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997083"
---
# <a name="glfrontface-function"></a><span data-ttu-id="e721f-104">glFrontFace función)</span><span class="sxs-lookup"><span data-stu-id="e721f-104">glFrontFace function</span></span>

<span data-ttu-id="e721f-105">La función **glFrontFace** define polígonos orientados delante y detrás.</span><span class="sxs-lookup"><span data-stu-id="e721f-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="e721f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e721f-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="e721f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e721f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e721f-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="e721f-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="e721f-109">Orientación de los polígonos orientados hacia delante.</span><span class="sxs-lookup"><span data-stu-id="e721f-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="e721f-110">\_Se aceptan GL CW y contabilidad \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="e721f-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="e721f-111">El valor predeterminado es el \_ CCW de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e721f-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e721f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e721f-112">Return value</span></span>

<span data-ttu-id="e721f-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e721f-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e721f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e721f-114">Error codes</span></span>

<span data-ttu-id="e721f-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e721f-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e721f-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e721f-116">Name</span></span>                                                                                                  | <span data-ttu-id="e721f-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e721f-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e721f-118"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e721f-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e721f-119">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="e721f-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="e721f-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e721f-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e721f-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e721f-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e721f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e721f-122">Remarks</span></span>

<span data-ttu-id="e721f-123">En una escena compuesta por completo de superficies cerradas opacas, los polígonos hacia delante nunca están visibles.</span><span class="sxs-lookup"><span data-stu-id="e721f-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="e721f-124">La eliminación de estos polígonos invisibles tiene la ventaja obvia de acelerar la representación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e721f-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="e721f-125">Puede habilitar y deshabilitar la eliminación de polígonos orientados al fondo con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) mediante el argumento de la cara de selección de libro de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e721f-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="e721f-126">Se dice que la proyección de un polígono a coordenadas de la ventana tiene un bobinado en el sentido de las agujas del reloj si un objeto imaginario que sigue a la ruta de acceso desde su primer vértice, su segundo vértice, etc., al último vértice y, finalmente, de nuevo al primer vértice, se mueve en sentido de las agujas del reloj sobre el interior del polígono.</span><span class="sxs-lookup"><span data-stu-id="e721f-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="e721f-127">Se dice que el bobinado del polígono está en sentido contrario a las agujas del reloj si el objeto imaginario que sigue a la misma ruta de acceso se mueve en sentido contrario a las agujas del reloj sobre el interior del polígono.</span><span class="sxs-lookup"><span data-stu-id="e721f-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="e721f-128">La función **glFrontFace** especifica si polígonos con el bobinado en el sentido de las agujas del reloj en las coordenadas de la ventana o el bobinado en sentido contrario a las agujas del reloj en coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e721f-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="e721f-129">Al pasar \_ el CCW de contabilidad al *modo* , se seleccionan los polígonos en sentido contrario a las agujas del reloj como anverso; GL \_ CW selecciona los polígonos en el sentido de las agujas del reloj como frontal.</span><span class="sxs-lookup"><span data-stu-id="e721f-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="e721f-130">De forma predeterminada, los polígonos en sentido contrario a las agujas del reloj se toman delante.</span><span class="sxs-lookup"><span data-stu-id="e721f-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="e721f-131">La siguiente función recupera información sobre **glFrontface**:</span><span class="sxs-lookup"><span data-stu-id="e721f-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="e721f-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ cara frontal de libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="e721f-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="e721f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e721f-133">Requirements</span></span>



| <span data-ttu-id="e721f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e721f-134">Requirement</span></span> | <span data-ttu-id="e721f-135">Value</span><span class="sxs-lookup"><span data-stu-id="e721f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e721f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e721f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e721f-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e721f-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e721f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e721f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e721f-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e721f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e721f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e721f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e721f-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e721f-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e721f-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e721f-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="e721f-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e721f-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e721f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e721f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e721f-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e721f-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e721f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e721f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e721f-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e721f-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e721f-148">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="e721f-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="e721f-149">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="e721f-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="e721f-150">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="e721f-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e721f-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e721f-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e721f-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e721f-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e721f-153">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="e721f-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





