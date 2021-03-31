---
title: función glClearStencil (GL. h)
description: La función glClearStencil especifica el valor sin cifrar para el búfer de estarcido.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glClearStencil (función) OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996528"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="77d9c-104">glClearStencil función)</span><span class="sxs-lookup"><span data-stu-id="77d9c-104">glClearStencil function</span></span>

<span data-ttu-id="77d9c-105">La función **glClearStencil** especifica el valor sin cifrar para el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="77d9c-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d9c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77d9c-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="77d9c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77d9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d9c-108">*s*</span><span class="sxs-lookup"><span data-stu-id="77d9c-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="77d9c-109">Índice que se utiliza cuando se borra el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="77d9c-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="77d9c-110">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="77d9c-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d9c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77d9c-111">Return value</span></span>

<span data-ttu-id="77d9c-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="77d9c-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77d9c-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="77d9c-113">Error codes</span></span>

<span data-ttu-id="77d9c-114">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="77d9c-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77d9c-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="77d9c-115">Name</span></span>                                                                                                  | <span data-ttu-id="77d9c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="77d9c-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77d9c-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77d9c-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77d9c-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="77d9c-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77d9c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77d9c-119">Remarks</span></span>

<span data-ttu-id="77d9c-120">La función **glClearStencil** especifica el índice usado por [**glClear**](glclear.md) para borrar el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="77d9c-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="77d9c-121">El parámetro *s* se enmascara con 2 <sup>m</sup>  -1, donde *m* es el número de bits en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="77d9c-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="77d9c-122">Las siguientes funciones recuperan información relacionada con la función **glClearStencil** :</span><span class="sxs-lookup"><span data-stu-id="77d9c-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="77d9c-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ GL \_ \_ valor sin formato de estarcido</span><span class="sxs-lookup"><span data-stu-id="77d9c-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="77d9c-124">**glGet** con el argumento \_ bits de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="77d9c-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="77d9c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d9c-125">Requirements</span></span>



| <span data-ttu-id="77d9c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d9c-126">Requirement</span></span> | <span data-ttu-id="77d9c-127">Value</span><span class="sxs-lookup"><span data-stu-id="77d9c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77d9c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77d9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="77d9c-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="77d9c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77d9c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77d9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="77d9c-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77d9c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77d9c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77d9c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d9c-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d9c-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77d9c-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77d9c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="77d9c-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77d9c-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77d9c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77d9c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77d9c-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77d9c-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d9c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="77d9c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d9c-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="77d9c-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77d9c-140">**glClear**</span><span class="sxs-lookup"><span data-stu-id="77d9c-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="77d9c-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="77d9c-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77d9c-142">**glGet**</span><span class="sxs-lookup"><span data-stu-id="77d9c-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





