---
title: función glRenderMode (GL. h)
description: La función glRenderMode establece el modo de rasterización.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode (función) OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151125"
---
# <a name="glrendermode-function"></a><span data-ttu-id="25d86-104">glRenderMode función)</span><span class="sxs-lookup"><span data-stu-id="25d86-104">glRenderMode function</span></span>

<span data-ttu-id="25d86-105">La función **glRenderMode** establece el modo de rasterización.</span><span class="sxs-lookup"><span data-stu-id="25d86-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d86-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25d86-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="25d86-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25d86-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25d86-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="25d86-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="25d86-109">Modo de rasterización.</span><span class="sxs-lookup"><span data-stu-id="25d86-109">The rasterization mode.</span></span> <span data-ttu-id="25d86-110">Se aceptan los siguientes tres valores.</span><span class="sxs-lookup"><span data-stu-id="25d86-110">The following three values are accepted.</span></span> <span data-ttu-id="25d86-111">El valor predeterminado es GL \_ Render.</span><span class="sxs-lookup"><span data-stu-id="25d86-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="25d86-112">Value</span><span class="sxs-lookup"><span data-stu-id="25d86-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="25d86-113">Significado</span><span class="sxs-lookup"><span data-stu-id="25d86-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="25d86-114"><dt>**representación en GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="25d86-115">Modo de representación.</span><span class="sxs-lookup"><span data-stu-id="25d86-115">Render mode.</span></span> <span data-ttu-id="25d86-116">Las primitivas se rasterizan, lo que produce fragmentos de píxeles, que se escriben en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="25d86-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="25d86-117">Este es el modo normal y también el modo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="25d86-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="25d86-118"><dt>**selección de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="25d86-119">Modo de selección.</span><span class="sxs-lookup"><span data-stu-id="25d86-119">Selection mode.</span></span> <span data-ttu-id="25d86-120">No se generan fragmentos de píxeles y no se realiza ningún cambio en el contenido de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="25d86-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="25d86-121">En su lugar, se devuelve un registro de los nombres de primitivas que se habrían dibujado si el modo de representación se \_ representase en GL en un búfer de selección, que se debe crear (vea [**glSelectBuffer**](glselectbuffer.md)) antes de que se escriba el modo de selección.</span><span class="sxs-lookup"><span data-stu-id="25d86-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="25d86-122"><dt>**Comentarios de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="25d86-123">Modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="25d86-123">Feedback mode.</span></span> <span data-ttu-id="25d86-124">No se generan fragmentos de píxeles y no se realiza ningún cambio en el contenido de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="25d86-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="25d86-125">En su lugar, las coordenadas y los atributos de los vértices que se habrían dibujado tenían el modo de representación \_ en GL se devuelve en un búfer de comentarios, que se debe crear (vea [**glFeedbackBuffer**](glfeedbackbuffer.md)) antes de que se escriba el modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="25d86-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="25d86-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="25d86-126">Error codes</span></span>

<span data-ttu-id="25d86-127">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="25d86-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="25d86-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="25d86-128">Name</span></span>                                                                                                  | <span data-ttu-id="25d86-129">Significado</span><span class="sxs-lookup"><span data-stu-id="25d86-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25d86-130"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="25d86-131">el *modo* no era uno de los tres valores aceptados.</span><span class="sxs-lookup"><span data-stu-id="25d86-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="25d86-132"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="25d86-133">Se llamó a la función con el argumento GL \_ Select antes de que se llamara a [**glSelectBuffer**](glselectbuffer.md) al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="25d86-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="25d86-134"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="25d86-135">Se llamó a la función con los comentarios de GL del argumento \_ antes de que se llamara a [**glBeedbackBuffer**](glfeedbackbuffer.md) al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="25d86-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="25d86-136"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="25d86-137">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="25d86-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="25d86-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25d86-138">Remarks</span></span>

<span data-ttu-id="25d86-139">La función **glRenderMode** toma un argumento, *mode*, que puede suponer uno de los tres valores predefinidos anteriores.</span><span class="sxs-lookup"><span data-stu-id="25d86-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="25d86-140">El valor devuelto de la función **glRenderMode** viene determinado por el modo de representación en el momento en que se llama a **glRenderMode** , en lugar de por el *modo*.</span><span class="sxs-lookup"><span data-stu-id="25d86-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="25d86-141">Los valores devueltos para los tres modos de representación son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="25d86-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="25d86-142">Value</span><span class="sxs-lookup"><span data-stu-id="25d86-142">Value</span></span>        | <span data-ttu-id="25d86-143">Significado</span><span class="sxs-lookup"><span data-stu-id="25d86-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="25d86-144">representación en GL \_</span><span class="sxs-lookup"><span data-stu-id="25d86-144">GL\_RENDER</span></span>   | <span data-ttu-id="25d86-145">Cero.</span><span class="sxs-lookup"><span data-stu-id="25d86-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="25d86-146">selección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="25d86-146">GL\_SELECT</span></span>   | <span data-ttu-id="25d86-147">El número de registros de aciertos transferidos al búfer seleccionado.</span><span class="sxs-lookup"><span data-stu-id="25d86-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="25d86-148">Comentarios de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="25d86-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="25d86-149">El número de valores (no los vértices) transferidos al búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="25d86-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="25d86-150">Consulte [**glSelectBuffer**](glselectbuffer.md) y [**glFeedbackBuffer**](glfeedbackbuffer.md) para obtener más detalles sobre la operación de selección y comentarios.</span><span class="sxs-lookup"><span data-stu-id="25d86-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="25d86-151">Si se genera un error, **glRenderMode** devuelve cero independientemente del modo de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="25d86-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="25d86-152">La siguiente función recupera información relacionada con **glRenderMode**:</span><span class="sxs-lookup"><span data-stu-id="25d86-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="25d86-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="25d86-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="25d86-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25d86-154">Requirements</span></span>



| <span data-ttu-id="25d86-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d86-155">Requirement</span></span> | <span data-ttu-id="25d86-156">Value</span><span class="sxs-lookup"><span data-stu-id="25d86-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25d86-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25d86-157">Minimum supported client</span></span><br/> | <span data-ttu-id="25d86-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="25d86-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="25d86-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25d86-159">Minimum supported server</span></span><br/> | <span data-ttu-id="25d86-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25d86-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25d86-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25d86-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="25d86-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="25d86-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25d86-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="25d86-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="25d86-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25d86-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25d86-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25d86-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25d86-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="25d86-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d86-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="25d86-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="25d86-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="25d86-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="25d86-170">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="25d86-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="25d86-171">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="25d86-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="25d86-172">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="25d86-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="25d86-173">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="25d86-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="25d86-174">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="25d86-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="25d86-175">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="25d86-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





