---
title: función glGetClipPlane (GL. h)
description: La función glGetClipPlane devuelve los coeficientes del plano de recorte especificado.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane (función) OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686251"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="97cb9-104">glGetClipPlane función)</span><span class="sxs-lookup"><span data-stu-id="97cb9-104">glGetClipPlane function</span></span>

<span data-ttu-id="97cb9-105">La función **glGetClipPlane** devuelve los coeficientes del plano de recorte especificado.</span><span class="sxs-lookup"><span data-stu-id="97cb9-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="97cb9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97cb9-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="97cb9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97cb9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97cb9-108">*plano*</span><span class="sxs-lookup"><span data-stu-id="97cb9-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="97cb9-109">Plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="97cb9-109">A clipping plane.</span></span> <span data-ttu-id="97cb9-110">El número de planos de recorte depende de la implementación, pero se admiten al menos seis planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="97cb9-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="97cb9-111">Se identifican por nombres simbólicos con el formato libro de clips de contabilidad \_ \_ *i* , donde 0 = *i* < \_ planos de \_ recortes de contab \_ .</span><span class="sxs-lookup"><span data-stu-id="97cb9-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="97cb9-112">*ecuación*</span><span class="sxs-lookup"><span data-stu-id="97cb9-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="97cb9-113">Devuelve cuatro valores de precisión doble que son los coeficientes de la ecuación de plano de *plano* en coordenadas de ojo.</span><span class="sxs-lookup"><span data-stu-id="97cb9-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97cb9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97cb9-114">Return value</span></span>

<span data-ttu-id="97cb9-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="97cb9-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97cb9-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="97cb9-116">Error codes</span></span>

<span data-ttu-id="97cb9-117">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="97cb9-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="97cb9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="97cb9-118">Name</span></span>                                                                                                  | <span data-ttu-id="97cb9-119">Significado</span><span class="sxs-lookup"><span data-stu-id="97cb9-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97cb9-120"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97cb9-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="97cb9-121">el *plano* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="97cb9-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="97cb9-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97cb9-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="97cb9-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="97cb9-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="97cb9-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97cb9-124">Remarks</span></span>

<span data-ttu-id="97cb9-125">La función **glGetClipPlane** devuelve en la *ecuación* los cuatro coeficientes de la ecuación del plano para el *plano*.</span><span class="sxs-lookup"><span data-stu-id="97cb9-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="97cb9-126">Siempre es el caso de que el \_ plano de clip GL \_ *i* = \_ recorte de GL \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="97cb9-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="97cb9-127">Si se genera un error, no se realiza ningún cambio en el contenido de la *ecuación*.</span><span class="sxs-lookup"><span data-stu-id="97cb9-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="97cb9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97cb9-128">Requirements</span></span>



| <span data-ttu-id="97cb9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="97cb9-129">Requirement</span></span> | <span data-ttu-id="97cb9-130">Value</span><span class="sxs-lookup"><span data-stu-id="97cb9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97cb9-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97cb9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="97cb9-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="97cb9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="97cb9-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97cb9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="97cb9-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97cb9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97cb9-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97cb9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="97cb9-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="97cb9-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="97cb9-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97cb9-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="97cb9-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97cb9-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="97cb9-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97cb9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97cb9-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97cb9-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97cb9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="97cb9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97cb9-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="97cb9-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="97cb9-143">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="97cb9-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="97cb9-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="97cb9-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





