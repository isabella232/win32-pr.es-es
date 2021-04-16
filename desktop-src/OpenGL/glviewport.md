---
title: función glViewport (GL. h)
description: La función glViewport establece la ventanilla.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport (función) OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104562016"
---
# <a name="glviewport-function"></a><span data-ttu-id="1b7ba-104">glViewport función)</span><span class="sxs-lookup"><span data-stu-id="1b7ba-104">glViewport function</span></span>

<span data-ttu-id="1b7ba-105">La función **glViewport** establece la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7ba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b7ba-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="1b7ba-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b7ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7ba-108">*x*</span><span class="sxs-lookup"><span data-stu-id="1b7ba-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="1b7ba-109">Esquina inferior izquierda del rectángulo de la ventanilla, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="1b7ba-110">El valor predeterminado es (0,0).</span><span class="sxs-lookup"><span data-stu-id="1b7ba-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="1b7ba-111">*y*</span><span class="sxs-lookup"><span data-stu-id="1b7ba-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="1b7ba-112">Esquina inferior izquierda del rectángulo de la ventanilla, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="1b7ba-113">El valor predeterminado es (0,0).</span><span class="sxs-lookup"><span data-stu-id="1b7ba-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="1b7ba-114">*width*</span><span class="sxs-lookup"><span data-stu-id="1b7ba-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="1b7ba-115">Ancho de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-115">The width of the viewport.</span></span> <span data-ttu-id="1b7ba-116">Cuando un contexto OpenGL se adjunta primero a una ventana, el *ancho* y el *alto* se establecen en las dimensiones de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ba-117">*height*</span><span class="sxs-lookup"><span data-stu-id="1b7ba-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="1b7ba-118">Alto de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-118">The height of the viewport.</span></span> <span data-ttu-id="1b7ba-119">Cuando un contexto OpenGL se adjunta primero a una ventana, el *ancho* y el *alto* se establecen en las dimensiones de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7ba-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b7ba-120">Return value</span></span>

<span data-ttu-id="1b7ba-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1b7ba-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1b7ba-122">Error codes</span></span>

<span data-ttu-id="1b7ba-123">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1b7ba-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b7ba-124">Name</span></span>                                                                                                  | <span data-ttu-id="1b7ba-125">Significado</span><span class="sxs-lookup"><span data-stu-id="1b7ba-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b7ba-126"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ba-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1b7ba-127">El *ancho* o el *alto* era negativo.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="1b7ba-128"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ba-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1b7ba-129">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1b7ba-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1b7ba-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b7ba-130">Remarks</span></span>

<span data-ttu-id="1b7ba-131">La función **glViewport** especifica la transformación afín de *x* e y desde las *coordenadas del dispositivo* normalizado a las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="1b7ba-132">Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) son coordenadas de dispositivo normalizadas.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="1b7ba-133">Las coordenadas de la ventana (*x*<sub>w</sub> , *y*<sub>w</sub> ) se calculan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1b7ba-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![Ecuación que muestra el cálculo de las coordenadas de la ventana.](images/view01.png)

<span data-ttu-id="1b7ba-135">El ancho y el alto de la ventanilla se fijan de forma silenciosa en un intervalo que depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="1b7ba-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="1b7ba-136">Este intervalo se consulta mediante una llamada a **glGet** con el argumento de la \_ ventanilla Max Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b7ba-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="1b7ba-137">Las siguientes funciones recuperan información relacionada con **glViewport**:</span><span class="sxs-lookup"><span data-stu-id="1b7ba-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="1b7ba-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ ventanilla de GL</span><span class="sxs-lookup"><span data-stu-id="1b7ba-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="1b7ba-139">**glGet** con el argumento \_ la \_ ventanilla Max Max \_ DiMS</span><span class="sxs-lookup"><span data-stu-id="1b7ba-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7ba-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b7ba-140">Requirements</span></span>



| <span data-ttu-id="1b7ba-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b7ba-141">Requirement</span></span> | <span data-ttu-id="1b7ba-142">Value</span><span class="sxs-lookup"><span data-stu-id="1b7ba-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7ba-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b7ba-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7ba-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1b7ba-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1b7ba-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b7ba-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7ba-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b7ba-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b7ba-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b7ba-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b7ba-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ba-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1b7ba-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b7ba-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b7ba-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ba-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b7ba-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b7ba-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b7ba-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ba-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b7ba-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b7ba-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7ba-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1b7ba-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1b7ba-155">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="1b7ba-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





