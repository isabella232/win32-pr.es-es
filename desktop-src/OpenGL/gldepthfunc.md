---
title: función glDepthFunc (GL. h)
description: La función glDepthFunc especifica el valor utilizado para las comparaciones de búfer de profundidad.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc (función) OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489736"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="1754a-104">glDepthFunc función)</span><span class="sxs-lookup"><span data-stu-id="1754a-104">glDepthFunc function</span></span>

<span data-ttu-id="1754a-105">La función **glDepthFunc** especifica el valor utilizado para las comparaciones de búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1754a-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="1754a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1754a-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="1754a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1754a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1754a-108">*func*</span><span class="sxs-lookup"><span data-stu-id="1754a-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="1754a-109">Especifica la función de comparación de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1754a-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="1754a-110">Se aceptan las siguientes constantes simbólicas.</span><span class="sxs-lookup"><span data-stu-id="1754a-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="1754a-111">Value</span><span class="sxs-lookup"><span data-stu-id="1754a-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="1754a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="1754a-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="1754a-113"><dt>**GL \_ nunca**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="1754a-114">Nunca pasa.</span><span class="sxs-lookup"><span data-stu-id="1754a-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="1754a-115"><dt>**CONTABILIDAD \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="1754a-116">Pasa si el valor *z* entrante es menor que el valor *z* almacenado.</span><span class="sxs-lookup"><span data-stu-id="1754a-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="1754a-117">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1754a-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="1754a-118"><dt>**GL \_ LEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="1754a-119">Pasa si el valor z entrante es menor o igual que el valor z almacenado.</span><span class="sxs-lookup"><span data-stu-id="1754a-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="1754a-120"><dt>**igual a GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="1754a-121">Pasa si el valor z entrante es igual al valor z almacenado.</span><span class="sxs-lookup"><span data-stu-id="1754a-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="1754a-122"><dt>**LIBRO \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="1754a-123">Pasa si el valor z entrante es mayor que el valor z almacenado.</span><span class="sxs-lookup"><span data-stu-id="1754a-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="1754a-124"><dt>**NOTEQUAL en GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="1754a-125">Pasa si el valor z entrante no es igual que el valor z almacenado.</span><span class="sxs-lookup"><span data-stu-id="1754a-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="1754a-126"><dt>**GL \_ GEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="1754a-127">Se pasa si el valor z entrante es mayor o igual que el valor z almacenado.</span><span class="sxs-lookup"><span data-stu-id="1754a-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="1754a-128"><dt>**GL \_ siempre**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="1754a-129">Siempre pasa.</span><span class="sxs-lookup"><span data-stu-id="1754a-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1754a-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1754a-130">Return value</span></span>

<span data-ttu-id="1754a-131">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1754a-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1754a-132">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1754a-132">Error codes</span></span>

<span data-ttu-id="1754a-133">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="1754a-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1754a-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="1754a-134">Name</span></span>                                                                                                  | <span data-ttu-id="1754a-135">Significado</span><span class="sxs-lookup"><span data-stu-id="1754a-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1754a-136"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1754a-137">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1754a-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1754a-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1754a-138">Remarks</span></span>

<span data-ttu-id="1754a-139">La función **glDepthFunc** especifica la función que se usa para comparar cada valor *z* de píxel entrante con el valor *z* presente en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1754a-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="1754a-140">La comparación se realiza solo si está habilitada la prueba de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1754a-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="1754a-141">(Consulte [**glEnable**](glenable.md) con el argumento GL \_ prueba de profundidad \_ ).</span><span class="sxs-lookup"><span data-stu-id="1754a-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="1754a-142">Inicialmente, las pruebas de profundidad están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="1754a-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="1754a-143">Las siguientes funciones recuperan información relacionada con **glDepthFunc**:</span><span class="sxs-lookup"><span data-stu-id="1754a-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="1754a-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de profundidad de libro de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="1754a-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="1754a-145">[**glIsEnabled**](glisenabled.md) con el argumento \_ prueba de profundidad de GL \_</span><span class="sxs-lookup"><span data-stu-id="1754a-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="1754a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1754a-146">Requirements</span></span>



| <span data-ttu-id="1754a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="1754a-147">Requirement</span></span> | <span data-ttu-id="1754a-148">Value</span><span class="sxs-lookup"><span data-stu-id="1754a-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1754a-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1754a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1754a-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1754a-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1754a-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1754a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1754a-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1754a-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1754a-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1754a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1754a-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1754a-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1754a-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="1754a-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1754a-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1754a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1754a-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1754a-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1754a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="1754a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1754a-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1754a-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1754a-161">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="1754a-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="1754a-162">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="1754a-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="1754a-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1754a-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1754a-164">**glGet**</span><span class="sxs-lookup"><span data-stu-id="1754a-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1754a-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1754a-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





