---
title: función glPointSize (GL. h)
description: La función glPointSize especifica el diámetro de los puntos rasterizados.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize (función) OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666024"
---
# <a name="glpointsize-function"></a><span data-ttu-id="a33b6-104">glPointSize función)</span><span class="sxs-lookup"><span data-stu-id="a33b6-104">glPointSize function</span></span>

<span data-ttu-id="a33b6-105">La función **glPointSize** especifica el diámetro de los puntos rasterizados.</span><span class="sxs-lookup"><span data-stu-id="a33b6-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33b6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a33b6-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="a33b6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a33b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33b6-108">*size*</span><span class="sxs-lookup"><span data-stu-id="a33b6-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="a33b6-109">Diámetro de los puntos rasterizados.</span><span class="sxs-lookup"><span data-stu-id="a33b6-109">The diameter of rasterized points.</span></span> <span data-ttu-id="a33b6-110">El valor predeterminado es 1.0.</span><span class="sxs-lookup"><span data-stu-id="a33b6-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33b6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a33b6-111">Return value</span></span>

<span data-ttu-id="a33b6-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a33b6-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a33b6-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a33b6-113">Error codes</span></span>

<span data-ttu-id="a33b6-114">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a33b6-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a33b6-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="a33b6-115">Name</span></span>                                                                                                  | <span data-ttu-id="a33b6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a33b6-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a33b6-117"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a33b6-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a33b6-118">*el tamaño* era menor o igual que cero.</span><span class="sxs-lookup"><span data-stu-id="a33b6-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="a33b6-119"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a33b6-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a33b6-120">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a33b6-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a33b6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a33b6-121">Remarks</span></span>

<span data-ttu-id="a33b6-122">La función **glPointSize** especifica el diámetro rasterizado de los puntos con alias y antialias.</span><span class="sxs-lookup"><span data-stu-id="a33b6-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="a33b6-123">El uso de un tamaño de punto distinto de 1,0 tiene efectos diferentes, en función de si está habilitado el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="a33b6-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="a33b6-124">El suavizado de contorno de punto se controla mediante una llamada a [**glEnable**](glenable.md) y **glDisable** con un argumento de punto de contabilidad \_ \_ suave.</span><span class="sxs-lookup"><span data-stu-id="a33b6-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="a33b6-125">Si el suavizado de contorno de punto está deshabilitado, el tamaño real se determina redondeando el tamaño proporcionado al entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="a33b6-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="a33b6-126">(Si el redondeo da como resultado el valor 0, es como si el tamaño del punto fuera 1). Si el tamaño redondeado es impar, el punto central (*x*,*y*) del fragmento de píxel que representa el punto se calcula como</span><span class="sxs-lookup"><span data-stu-id="a33b6-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="a33b6-127">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> + 5)</span><span class="sxs-lookup"><span data-stu-id="a33b6-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="a33b6-128">donde *w* los subíndices indican las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a33b6-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="a33b6-129">Todos los píxeles que se encuentran dentro de la cuadrícula cuadrada del tamaño redondeado centrado en (*x*,*y*) componen el fragmento.</span><span class="sxs-lookup"><span data-stu-id="a33b6-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="a33b6-130">Si el tamaño es par, el punto central es</span><span class="sxs-lookup"><span data-stu-id="a33b6-130">If the size is even, the center point is</span></span>

<span data-ttu-id="a33b6-131">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> + 5)</span><span class="sxs-lookup"><span data-stu-id="a33b6-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="a33b6-132">y los centros del fragmento rasterizado son las coordenadas de la ventana de medio entero dentro del cuadrado del tamaño redondeado centrado en (*x*,*y*).</span><span class="sxs-lookup"><span data-stu-id="a33b6-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="a33b6-133">A todos los fragmentos de píxeles producidos en la rasterización de un punto nonantialiased se les asignan los mismos datos asociados. del vértice correspondiente al punto.</span><span class="sxs-lookup"><span data-stu-id="a33b6-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="a33b6-134">Si el suavizado de contorno está habilitado, la rasterización de puntos produce un fragmento para cada cuadrado de píxeles que forma una intersección con la región en el círculo que tiene un diámetro igual al tamaño de punto actual y se centra en los puntos (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span><span class="sxs-lookup"><span data-stu-id="a33b6-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="a33b6-135">El valor de cobertura de cada fragmento es el área de coordenadas de la ventana de la intersección de la región circular con el cuadrado de píxeles correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a33b6-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="a33b6-136">Este valor se guarda y se usa en el paso de rasterización final.</span><span class="sxs-lookup"><span data-stu-id="a33b6-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="a33b6-137">Los datos asociados a cada fragmento son los datos asociados con el punto que se va a Rasterizar.</span><span class="sxs-lookup"><span data-stu-id="a33b6-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="a33b6-138">No se admiten todos los tamaños cuando está habilitado el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="a33b6-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="a33b6-139">Si se solicita un tamaño no compatible, se usa el tamaño admitido más cercano.</span><span class="sxs-lookup"><span data-stu-id="a33b6-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="a33b6-140">Solo se garantiza que el tamaño 1,0 es compatible; otros dependen de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a33b6-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="a33b6-141">El intervalo de tamaños admitidos y la diferencia de tamaño entre los tamaños admitidos en el intervalo se pueden consultar mediante una llamada a [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con los argumentos de \_ intervalo de \_ tamaño de punto de contabilidad \_ y granularidad de tamaño de punto de contabilidad \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a33b6-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="a33b6-142">Siempre se devuelve el tamaño de punto especificado por **glPointSize** cuando \_ se consulta el tamaño de los puntos de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="a33b6-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="a33b6-143">La compresión y el redondeo de los puntos con alias y sin alias no tienen ningún efecto en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a33b6-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="a33b6-144">El tamaño de los puntos sin alias se puede fijar en un máximo dependiente de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a33b6-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="a33b6-145">Aunque no se puede consultar este máximo, no debe ser menor que el valor máximo de los puntos alisados, redondeado al valor entero más cercano.</span><span class="sxs-lookup"><span data-stu-id="a33b6-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="a33b6-146">Las siguientes funciones recuperan información relacionada con **glPointSize**:</span><span class="sxs-lookup"><span data-stu-id="a33b6-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="a33b6-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de tamaño de los puntos de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="a33b6-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="a33b6-148">**glGet** con \_ \_ el intervalo de tamaño de punto de contabilidad de argumento \_</span><span class="sxs-lookup"><span data-stu-id="a33b6-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="a33b6-149">**glGet** con granularidad de \_ tamaño de punto de contabilidad de argumento \_ \_</span><span class="sxs-lookup"><span data-stu-id="a33b6-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="a33b6-150">[**glIsEnabled**](glisenabled.md) con un argumento de punto de contabilidad \_ \_ suave</span><span class="sxs-lookup"><span data-stu-id="a33b6-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="a33b6-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33b6-151">Requirements</span></span>



| <span data-ttu-id="a33b6-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33b6-152">Requirement</span></span> | <span data-ttu-id="a33b6-153">Value</span><span class="sxs-lookup"><span data-stu-id="a33b6-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a33b6-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33b6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a33b6-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a33b6-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a33b6-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33b6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a33b6-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a33b6-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a33b6-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a33b6-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33b6-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33b6-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a33b6-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a33b6-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="a33b6-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a33b6-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a33b6-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a33b6-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a33b6-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33b6-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33b6-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="a33b6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33b6-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a33b6-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a33b6-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="a33b6-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="a33b6-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a33b6-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a33b6-168">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a33b6-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





