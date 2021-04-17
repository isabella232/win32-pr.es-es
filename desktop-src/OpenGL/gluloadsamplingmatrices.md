---
title: función gluLoadSamplingMatrices (GLU. h)
description: La función gluLoadSamplingMatrices carga las matrices de muestreo y selección de la spline B-spline racional (NURBS) no uniformes.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices (función) OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665953"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="f5240-104">gluLoadSamplingMatrices función)</span><span class="sxs-lookup"><span data-stu-id="f5240-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="f5240-105">La función **gluLoadSamplingMatrices** carga las matrices de muestreo y selección de la spline B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniformes.</span><span class="sxs-lookup"><span data-stu-id="f5240-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5240-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5240-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="f5240-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5240-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5240-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="f5240-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="f5240-109">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="f5240-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f5240-110">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="f5240-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="f5240-111">Matriz MODELVIEW (a partir de una llamada a [**glGetFloatv**](glgetfloatv.md) ).</span><span class="sxs-lookup"><span data-stu-id="f5240-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="f5240-112">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="f5240-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="f5240-113">Matriz de proyección (a partir de una llamada a **glGetFloatv** ).</span><span class="sxs-lookup"><span data-stu-id="f5240-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="f5240-114">*encuadre*</span><span class="sxs-lookup"><span data-stu-id="f5240-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="f5240-115">Una ventanilla (a partir de una llamada a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="f5240-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5240-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5240-116">Return value</span></span>

<span data-ttu-id="f5240-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f5240-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5240-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5240-118">Remarks</span></span>

<span data-ttu-id="f5240-119">La función **gluLoadSamplingMatrices** usa *modelMatrix*, *projMatrix* y *viewport* para volver a calcular las matrices de muestreo y selección almacenadas en *nobj*.</span><span class="sxs-lookup"><span data-stu-id="f5240-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="f5240-120">La matriz de muestreo determina la precisión con que una curva o superficie de NURBS debe ser teselada para satisfacer la tolerancia de muestreo (según lo determinado por la propiedad de tolerancia de muestreo de GLU \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="f5240-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="f5240-121">La matriz de selección se usa para decidir si se debe seleccionar una curva o superficie de NURBS antes de la representación (cuando la \_ propiedad de selección de Glu está activada).</span><span class="sxs-lookup"><span data-stu-id="f5240-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="f5240-122">La función **gluLoadSamplingMatrices** solo es necesaria si la propiedad de la matriz de carga automática Glu está desactivada \_ \_ \_ (consulte [**gluNurbsProperty**](glunurbsproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="f5240-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="f5240-123">Aunque puede ser conveniente dejar \_ \_ activada la \_ propiedad de matriz de carga automática de Glu, al hacerlo se requiere un recorrido de ida y vuelta al servidor de OpenGL para obtener los valores actuales de la matriz de MODELVIEW, la matriz de proyección y la ventanilla).</span><span class="sxs-lookup"><span data-stu-id="f5240-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="f5240-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5240-124">Requirements</span></span>



| <span data-ttu-id="f5240-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5240-125">Requirement</span></span> | <span data-ttu-id="f5240-126">Value</span><span class="sxs-lookup"><span data-stu-id="f5240-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5240-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5240-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5240-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5240-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f5240-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5240-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5240-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5240-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f5240-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5240-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5240-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5240-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f5240-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5240-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5240-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5240-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5240-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5240-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5240-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5240-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5240-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5240-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5240-138">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="f5240-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="f5240-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f5240-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f5240-140">**gluGetNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="f5240-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="f5240-141">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="f5240-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





