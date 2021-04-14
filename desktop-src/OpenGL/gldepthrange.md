---
title: función glDepthRange (GL. h)
description: La función glDepthRange especifica la asignación de valores z de coordenadas de dispositivo normalizadas a coordenadas de la ventana.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange (función) OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422111"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="6133e-104">glDepthRange función)</span><span class="sxs-lookup"><span data-stu-id="6133e-104">glDepthRange function</span></span>

<span data-ttu-id="6133e-105">La función **glDepthRange** especifica la asignación de valores *z* de coordenadas de dispositivo normalizadas a coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6133e-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6133e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6133e-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="6133e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6133e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6133e-108">*zNear*</span><span class="sxs-lookup"><span data-stu-id="6133e-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="6133e-109">Asignación del plano de recorte cercano a las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6133e-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="6133e-110">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="6133e-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="6133e-111">*zFar*</span><span class="sxs-lookup"><span data-stu-id="6133e-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="6133e-112">Asignación del plano de recorte lejano a las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6133e-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="6133e-113">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="6133e-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6133e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6133e-114">Return value</span></span>

<span data-ttu-id="6133e-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6133e-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6133e-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6133e-116">Error codes</span></span>

<span data-ttu-id="6133e-117">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="6133e-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6133e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6133e-118">Name</span></span>                                                                                                  | <span data-ttu-id="6133e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="6133e-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6133e-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6133e-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6133e-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6133e-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6133e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6133e-122">Remarks</span></span>

<span data-ttu-id="6133e-123">Después del recorte y la división por *w*, las coordenadas *z* van de 0,0 a 1,0, correspondientes a los planos de recorte Near y Far.</span><span class="sxs-lookup"><span data-stu-id="6133e-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="6133e-124">La función **glDepthRange** especifica una asignación lineal de las coordenadas *z* normalizadas en este intervalo a las coordenadas *z* de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6133e-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="6133e-125">Independientemente de la implementación del búfer de profundidad real, los valores de profundidad de coordenadas de la ventana se tratan como si fueran de 0,0 a 1,0 (como los componentes de color).</span><span class="sxs-lookup"><span data-stu-id="6133e-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="6133e-126">Por lo tanto, los valores aceptados por **glDepthRange** se fijan a este intervalo antes de aceptarlos.</span><span class="sxs-lookup"><span data-stu-id="6133e-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="6133e-127">La asignación predeterminada de (0,0) asigna el plano cercano a 0 y el plano lejano a 1.</span><span class="sxs-lookup"><span data-stu-id="6133e-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="6133e-128">Con esta asignación, el intervalo de búfer de profundidad se ha utilizado por completo.</span><span class="sxs-lookup"><span data-stu-id="6133e-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="6133e-129">No es necesario que *zNear* sea menor que *zFar*.</span><span class="sxs-lookup"><span data-stu-id="6133e-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="6133e-130">Las asignaciones inversas como (1,0) son aceptables.</span><span class="sxs-lookup"><span data-stu-id="6133e-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="6133e-131">La siguiente función recupera información relacionada con **glDepthRange**:</span><span class="sxs-lookup"><span data-stu-id="6133e-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="6133e-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con rango de profundidad de contabilidad de argumentos \_ \_</span><span class="sxs-lookup"><span data-stu-id="6133e-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="6133e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6133e-133">Requirements</span></span>



| <span data-ttu-id="6133e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6133e-134">Requirement</span></span> | <span data-ttu-id="6133e-135">Value</span><span class="sxs-lookup"><span data-stu-id="6133e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6133e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6133e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6133e-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6133e-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6133e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6133e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6133e-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6133e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6133e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6133e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6133e-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6133e-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6133e-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6133e-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="6133e-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6133e-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6133e-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6133e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6133e-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6133e-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6133e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="6133e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6133e-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6133e-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6133e-148">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="6133e-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="6133e-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6133e-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6133e-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="6133e-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6133e-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="6133e-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





