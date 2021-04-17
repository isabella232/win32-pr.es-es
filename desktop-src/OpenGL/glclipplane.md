---
title: función glClipPlane (GL. h)
description: La función glClipPlane especifica un plano en el que se recorta todo el objeto Geometry.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane (función) OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686044"
---
# <a name="glclipplane-function"></a><span data-ttu-id="9851e-104">glClipPlane función)</span><span class="sxs-lookup"><span data-stu-id="9851e-104">glClipPlane function</span></span>

<span data-ttu-id="9851e-105">La función **glClipPlane** especifica un plano en el que se recorta todo el objeto Geometry.</span><span class="sxs-lookup"><span data-stu-id="9851e-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="9851e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9851e-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="9851e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9851e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9851e-108">*plano*</span><span class="sxs-lookup"><span data-stu-id="9851e-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="9851e-109">Plano de recorte que se está colocando.</span><span class="sxs-lookup"><span data-stu-id="9851e-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="9851e-110">Los nombres simbólicos del formulario de clip de contab \_ \_ .*i*, donde *i* es un entero entre 0 y el \_ número máximo \_ \_ de planos de clips-1, se aceptan.</span><span class="sxs-lookup"><span data-stu-id="9851e-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9851e-111">*ecuación*</span><span class="sxs-lookup"><span data-stu-id="9851e-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="9851e-112">Dirección de una matriz de cuatro valores de punto flotante de precisión doble.</span><span class="sxs-lookup"><span data-stu-id="9851e-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="9851e-113">Estos valores se interpretan como una ecuación de plano.</span><span class="sxs-lookup"><span data-stu-id="9851e-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9851e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9851e-114">Return value</span></span>

<span data-ttu-id="9851e-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9851e-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9851e-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9851e-116">Error codes</span></span>

<span data-ttu-id="9851e-117">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="9851e-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9851e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9851e-118">Name</span></span>                                                                                                  | <span data-ttu-id="9851e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="9851e-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9851e-120"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9851e-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9851e-121">el *plano* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="9851e-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="9851e-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9851e-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9851e-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9851e-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9851e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9851e-124">Remarks</span></span>

<span data-ttu-id="9851e-125">Geometry siempre se recorta con respecto a los límites de un frustum de seis planos en *x*, *y* y *z*.</span><span class="sxs-lookup"><span data-stu-id="9851e-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="9851e-126">La función **glClipPlane** permite la especificación de planos adicionales, no necesariamente perpendiculares al eje *x*, eje *y*, o eje *z*, en el que se recortan todas las geometrías.</span><span class="sxs-lookup"><span data-stu-id="9851e-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="9851e-127">Se \_ pueden especificar los planos de planos de recortes hasta un máximo de GL \_ \_ , donde \_ los planos de clip Max de GL \_ \_ son al menos seis en todas las implementaciones.</span><span class="sxs-lookup"><span data-stu-id="9851e-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="9851e-128">Dado que la región de recorte resultante es la intersección de los semiespacios definidos, siempre es convexa.</span><span class="sxs-lookup"><span data-stu-id="9851e-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="9851e-129">La función **glClipPlane** especifica un medio de espacio mediante una ecuación de plano de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="9851e-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="9851e-130">Cuando se llama a **glClipPlane**, la *ecuación* se transforma por el inverso de la matriz MODELVIEW y se almacena en las coordenadas de ojo resultantes.</span><span class="sxs-lookup"><span data-stu-id="9851e-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="9851e-131">Los cambios subsiguientes en la matriz MODELVIEW no tienen ningún efecto en los componentes de la ecuación de plano almacenados.</span><span class="sxs-lookup"><span data-stu-id="9851e-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="9851e-132">Si el producto del punto de las coordenadas del ojo de un vértice con los componentes de la ecuación de plano almacenado es positivo o cero, el vértice está en con respecto a ese plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="9851e-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="9851e-133">De lo contrario, está fuera.</span><span class="sxs-lookup"><span data-stu-id="9851e-133">Otherwise, it is out.</span></span>

<span data-ttu-id="9851e-134">Use las funciones [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) para habilitar y deshabilitar los planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="9851e-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="9851e-135">Llame a los planos de recorte con el argumento GL \_ clip \_ plano *i*, donde *i* es el número de plano.</span><span class="sxs-lookup"><span data-stu-id="9851e-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="9851e-136">De forma predeterminada, todos los planos de recorte se definen como (0, 0, 0, 0) en las coordenadas de ojo y están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="9851e-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="9851e-137">Siempre es el caso de que el \_ plano de clip GL \_ *i* = \_ recorte de GL \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="9851e-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="9851e-138">Las siguientes funciones recuperan información relacionada con **glClipPlane**:</span><span class="sxs-lookup"><span data-stu-id="9851e-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="9851e-139">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="9851e-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="9851e-140">[**glIsEnabled**](glisenabled.md) con el argumento \_ plano de clip de contabilidad \_ </span><span class="sxs-lookup"><span data-stu-id="9851e-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="9851e-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9851e-141">Requirements</span></span>



| <span data-ttu-id="9851e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9851e-142">Requirement</span></span> | <span data-ttu-id="9851e-143">Value</span><span class="sxs-lookup"><span data-stu-id="9851e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9851e-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9851e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9851e-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9851e-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9851e-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9851e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9851e-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9851e-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9851e-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9851e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9851e-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9851e-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9851e-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9851e-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="9851e-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9851e-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9851e-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9851e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9851e-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9851e-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9851e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="9851e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9851e-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9851e-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9851e-156">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="9851e-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="9851e-157">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9851e-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9851e-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9851e-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9851e-159">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="9851e-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="9851e-160">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="9851e-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





