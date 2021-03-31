---
title: función glPassThrough (GL. h)
description: La función glPassThrough coloca un marcador en el búfer de comentarios.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough (función) OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802000"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="e4ff6-104">glPassThrough función)</span><span class="sxs-lookup"><span data-stu-id="e4ff6-104">glPassThrough function</span></span>

<span data-ttu-id="e4ff6-105">La función **glPassThrough** coloca un marcador en el búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ff6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4ff6-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="e4ff6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4ff6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ff6-108">*token*</span><span class="sxs-lookup"><span data-stu-id="e4ff6-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="e4ff6-109">Un valor de marcador que se va a colocar en el búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="e4ff6-110">Se indica con el siguiente valor de identificación único.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="e4ff6-111">Value</span><span class="sxs-lookup"><span data-stu-id="e4ff6-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="e4ff6-112">Significado</span><span class="sxs-lookup"><span data-stu-id="e4ff6-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="e4ff6-113"><dt>**\_token de paso \_ a través de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4ff6-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="e4ff6-114">Se mantiene el orden de los comandos **glPassThrough** con respecto a la especificación de primitivas de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ff6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4ff6-115">Return value</span></span>

<span data-ttu-id="e4ff6-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4ff6-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e4ff6-117">Error codes</span></span>

<span data-ttu-id="e4ff6-118">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e4ff6-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4ff6-119">Name</span></span>                                                                                                  | <span data-ttu-id="e4ff6-120">Significado</span><span class="sxs-lookup"><span data-stu-id="e4ff6-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4ff6-121"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4ff6-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e4ff6-122">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e4ff6-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4ff6-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4ff6-123">Remarks</span></span>

<span data-ttu-id="e4ff6-124">Feedback es un modo de representación de OpenGL seleccionado llamando a [**glRenderMode**](glrendermode.md) con comentarios de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="e4ff6-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="e4ff6-125">Cuando OpenGL está en modo de comentarios, no se genera ningún píxel mediante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="e4ff6-126">En su lugar, la información acerca de los primitivos que se habrían rasterizado se devolverá a la aplicación mediante OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="e4ff6-127">Vea [**glFeedbackBuffer**](glfeedbackbuffer.md) para obtener una descripción del búfer de comentarios y los valores que hay en él.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="e4ff6-128">La función **glPassThrough** inserta un marcador definido por el usuario en el búfer de comentarios cuando se ejecuta en modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="e4ff6-129">El parámetro *token* se devuelve como si fuera un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="e4ff6-130">La función **glPassThrough** se omite si OpenGL no está en modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="e4ff6-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="e4ff6-131">La siguiente función recupera información relacionada con **glPassThrough**:</span><span class="sxs-lookup"><span data-stu-id="e4ff6-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="e4ff6-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="e4ff6-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ff6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4ff6-133">Requirements</span></span>



| <span data-ttu-id="e4ff6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ff6-134">Requirement</span></span> | <span data-ttu-id="e4ff6-135">Value</span><span class="sxs-lookup"><span data-stu-id="e4ff6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ff6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4ff6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ff6-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4ff6-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4ff6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4ff6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ff6-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4ff6-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4ff6-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4ff6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4ff6-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4ff6-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e4ff6-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4ff6-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4ff6-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4ff6-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e4ff6-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4ff6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4ff6-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4ff6-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ff6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4ff6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ff6-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e4ff6-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e4ff6-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e4ff6-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e4ff6-149">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="e4ff6-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="e4ff6-150">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="e4ff6-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





