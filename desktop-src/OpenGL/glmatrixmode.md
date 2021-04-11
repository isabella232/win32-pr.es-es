---
title: función glMatrixMode (GL. h)
description: La función glMatrixMode especifica qué matriz es la matriz actual.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode (función) OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150619"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="2eba0-104">glMatrixMode función)</span><span class="sxs-lookup"><span data-stu-id="2eba0-104">glMatrixMode function</span></span>

<span data-ttu-id="2eba0-105">La función **glMatrixMode** especifica qué matriz es la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="2eba0-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eba0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eba0-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="2eba0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eba0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eba0-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="2eba0-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="2eba0-109">Pila de matriz que es el destino de las operaciones de matriz posteriores.</span><span class="sxs-lookup"><span data-stu-id="2eba0-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="2eba0-110">El parámetro de *modo* puede suponer uno de los tres valores.</span><span class="sxs-lookup"><span data-stu-id="2eba0-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="2eba0-111">Value</span><span class="sxs-lookup"><span data-stu-id="2eba0-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="2eba0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="2eba0-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="2eba0-113"><dt>**GL \_ MODELVIEW**</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="2eba0-114">Aplica las operaciones de matriz subsiguientes a la pila de matriz de MODELVIEW.</span><span class="sxs-lookup"><span data-stu-id="2eba0-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="2eba0-115"><dt>**\_proyección GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="2eba0-116">Aplica las operaciones de matriz subsiguientes a la pila de la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="2eba0-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="2eba0-117"><dt>**\_textura GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="2eba0-118">Aplica las operaciones de matriz subsiguientes a la pila de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="2eba0-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eba0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eba0-119">Return value</span></span>

<span data-ttu-id="2eba0-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2eba0-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2eba0-121">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2eba0-121">Error codes</span></span>

<span data-ttu-id="2eba0-122">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="2eba0-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2eba0-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="2eba0-123">Name</span></span>                                                                                                  | <span data-ttu-id="2eba0-124">Significado</span><span class="sxs-lookup"><span data-stu-id="2eba0-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2eba0-125"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2eba0-126">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="2eba0-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="2eba0-127"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2eba0-128">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2eba0-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2eba0-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2eba0-129">Remarks</span></span>

<span data-ttu-id="2eba0-130">La función **glMatrixMode** establece el modo de matriz actual.</span><span class="sxs-lookup"><span data-stu-id="2eba0-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="2eba0-131">La siguiente función recupera información relacionada con **glMatrixMode**:</span><span class="sxs-lookup"><span data-stu-id="2eba0-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="2eba0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="2eba0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="2eba0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eba0-133">Requirements</span></span>



| <span data-ttu-id="2eba0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eba0-134">Requirement</span></span> | <span data-ttu-id="2eba0-135">Value</span><span class="sxs-lookup"><span data-stu-id="2eba0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eba0-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eba0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2eba0-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2eba0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2eba0-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eba0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2eba0-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2eba0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2eba0-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2eba0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eba0-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2eba0-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2eba0-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="2eba0-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2eba0-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2eba0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eba0-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eba0-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eba0-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eba0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eba0-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2eba0-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2eba0-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2eba0-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2eba0-149">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="2eba0-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="2eba0-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="2eba0-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





