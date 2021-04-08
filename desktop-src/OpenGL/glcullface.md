---
title: función glCullFace (GL. h)
description: La función glCullFace especifica si se pueden seleccionar las caras con conexión frontal o hacia delante.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace (función) OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996043"
---
# <a name="glcullface-function"></a><span data-ttu-id="ec641-104">glCullFace función)</span><span class="sxs-lookup"><span data-stu-id="ec641-104">glCullFace function</span></span>

<span data-ttu-id="ec641-105">La función **glCullFace** especifica si se pueden seleccionar las caras con conexión frontal o hacia delante.</span><span class="sxs-lookup"><span data-stu-id="ec641-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec641-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec641-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ec641-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec641-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec641-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="ec641-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ec641-109">Especifica si las caras delanteras o las orientadas hacia atrás son candidatas para la selección.</span><span class="sxs-lookup"><span data-stu-id="ec641-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="ec641-110">Se aceptan las constantes simbólicas GL \_ Front, GL \_ back y GL \_ Front \_ y \_ back.</span><span class="sxs-lookup"><span data-stu-id="ec641-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="ec641-111">El valor predeterminado es GL \_ .</span><span class="sxs-lookup"><span data-stu-id="ec641-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec641-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec641-112">Return value</span></span>

<span data-ttu-id="ec641-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec641-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec641-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ec641-114">Error codes</span></span>

<span data-ttu-id="ec641-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="ec641-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ec641-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec641-116">Name</span></span>                                                                                                  | <span data-ttu-id="ec641-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ec641-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec641-118"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ec641-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ec641-119">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="ec641-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="ec641-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ec641-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ec641-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ec641-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ec641-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec641-122">Remarks</span></span>

<span data-ttu-id="ec641-123">La función **glCullFace** especifica si se seleccionan las facetas con conexión frontal o hacia delante (como se especifica en el *modo*) cuando está habilitada la selección de facetas.</span><span class="sxs-lookup"><span data-stu-id="ec641-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="ec641-124">Puede habilitar y deshabilitar la selección de facetas mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento de la cara de selección de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ec641-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="ec641-125">Las caras incluyen triángulos, quadrilaterals, polígonos y rectángulos.</span><span class="sxs-lookup"><span data-stu-id="ec641-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="ec641-126">La función [**glFrontFace**](glfrontface.md) especifica cuál de las caras en el sentido de las agujas del reloj y en el sentido de las agujas del reloj está orientada hacia delante y hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="ec641-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="ec641-127">Si el *modo* es de \_ primer plano \_ y \_ viceversa, no se dibujan las caras, pero se dibujan otras primitivas, como puntos y líneas.</span><span class="sxs-lookup"><span data-stu-id="ec641-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="ec641-128">Las siguientes funciones recuperan información relacionada con **glCullFace**:</span><span class="sxs-lookup"><span data-stu-id="ec641-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="ec641-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de \_ cara de selección de libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="ec641-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="ec641-130">[**glIsEnabled**](glisenabled.md) con el argumento de la cara de selección de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec641-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="ec641-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec641-131">Requirements</span></span>



| <span data-ttu-id="ec641-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec641-132">Requirement</span></span> | <span data-ttu-id="ec641-133">Value</span><span class="sxs-lookup"><span data-stu-id="ec641-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec641-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec641-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ec641-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ec641-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ec641-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec641-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ec641-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec641-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec641-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec641-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec641-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec641-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ec641-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec641-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec641-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec641-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ec641-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec641-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec641-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec641-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec641-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec641-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec641-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ec641-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ec641-146">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="ec641-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="ec641-147">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="ec641-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="ec641-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ec641-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ec641-149">**glFrontFace**</span><span class="sxs-lookup"><span data-stu-id="ec641-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="ec641-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ec641-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ec641-151">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ec641-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





