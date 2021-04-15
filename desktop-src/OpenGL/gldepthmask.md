---
title: función glDepthMask (GL. h)
description: La función glDepthMask habilita o deshabilita la escritura en el búfer de profundidad.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- glDepthMask (función) OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422392"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="684ed-104">glDepthMask función)</span><span class="sxs-lookup"><span data-stu-id="684ed-104">glDepthMask function</span></span>

<span data-ttu-id="684ed-105">La función **glDepthMask** habilita o deshabilita la escritura en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="684ed-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="684ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="684ed-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="684ed-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="684ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="684ed-108">*flag*</span><span class="sxs-lookup"><span data-stu-id="684ed-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="684ed-109">Especifica si el búfer de profundidad está habilitado para escritura.</span><span class="sxs-lookup"><span data-stu-id="684ed-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="684ed-110">Si la *marca* es cero, la escritura de búfer de profundidad está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="684ed-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="684ed-111">De lo contrario, se habilita.</span><span class="sxs-lookup"><span data-stu-id="684ed-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="684ed-112">Inicialmente, la escritura de búfer de profundidad está habilitada.</span><span class="sxs-lookup"><span data-stu-id="684ed-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="684ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="684ed-113">Return value</span></span>

<span data-ttu-id="684ed-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="684ed-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="684ed-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="684ed-115">Error codes</span></span>

<span data-ttu-id="684ed-116">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="684ed-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="684ed-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="684ed-117">Name</span></span>                                                                                                  | <span data-ttu-id="684ed-118">Significado</span><span class="sxs-lookup"><span data-stu-id="684ed-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="684ed-119"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="684ed-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="684ed-120">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="684ed-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="684ed-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="684ed-121">Remarks</span></span>

<span data-ttu-id="684ed-122">La siguiente función recupera información relacionada con **glDepthMask**:</span><span class="sxs-lookup"><span data-stu-id="684ed-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="684ed-123">**glGet** con el argumento \_ profundidad de GL \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="684ed-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="684ed-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="684ed-124">Requirements</span></span>



| <span data-ttu-id="684ed-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="684ed-125">Requirement</span></span> | <span data-ttu-id="684ed-126">Value</span><span class="sxs-lookup"><span data-stu-id="684ed-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="684ed-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="684ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="684ed-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="684ed-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="684ed-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="684ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="684ed-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="684ed-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="684ed-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="684ed-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="684ed-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="684ed-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="684ed-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="684ed-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="684ed-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="684ed-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="684ed-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="684ed-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="684ed-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="684ed-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684ed-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="684ed-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684ed-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="684ed-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="684ed-139">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="684ed-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="684ed-140">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="684ed-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="684ed-141">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="684ed-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="684ed-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="684ed-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="684ed-143">**glGet**</span><span class="sxs-lookup"><span data-stu-id="684ed-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="684ed-144">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="684ed-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="684ed-145">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="684ed-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





