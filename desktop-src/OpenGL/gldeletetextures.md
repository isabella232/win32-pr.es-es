---
title: función glDeleteTextures (GL. h)
description: La función glDeleteTextures elimina las texturas con nombre.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- glDeleteTextures (función) OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489568"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="4a088-104">glDeleteTextures función)</span><span class="sxs-lookup"><span data-stu-id="4a088-104">glDeleteTextures function</span></span>

<span data-ttu-id="4a088-105">La función **glDeleteTextures** elimina las texturas con nombre.</span><span class="sxs-lookup"><span data-stu-id="4a088-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a088-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a088-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="4a088-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a088-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a088-108">*n*</span><span class="sxs-lookup"><span data-stu-id="4a088-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="4a088-109">Número de texturas que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="4a088-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="4a088-110">*texturas*</span><span class="sxs-lookup"><span data-stu-id="4a088-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="4a088-111">Matriz de texturas que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="4a088-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a088-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a088-112">Return value</span></span>

<span data-ttu-id="4a088-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4a088-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4a088-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4a088-114">Error codes</span></span>

<span data-ttu-id="4a088-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="4a088-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4a088-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a088-116">Name</span></span>                                                                                                  | <span data-ttu-id="4a088-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4a088-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a088-118"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a088-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="4a088-119">*n* era un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="4a088-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="4a088-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a088-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4a088-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4a088-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4a088-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a088-122">Remarks</span></span>

<span data-ttu-id="4a088-123">La función **glDeleteTextures** elimina *n* texturas denominadas por los elementos de las *texturas* de la matriz.</span><span class="sxs-lookup"><span data-stu-id="4a088-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="4a088-124">Una vez eliminada una textura, no tiene contenido ni dimensionalidad, y su nombre es gratuito para su reutilización (por ejemplo, por **glGenTextures**).</span><span class="sxs-lookup"><span data-stu-id="4a088-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="4a088-125">La función **glDeleteTextures** omite los ceros y los nombres que no se corresponden con las texturas existentes.</span><span class="sxs-lookup"><span data-stu-id="4a088-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="4a088-126">Si se elimina una textura enlazada actualmente, el enlace vuelve a cero (la textura predeterminada).</span><span class="sxs-lookup"><span data-stu-id="4a088-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="4a088-127">No puede incluir llamadas a **glDeleteTextures** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="4a088-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="4a088-128">La función **glDeleteTextures** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4a088-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="4a088-129">La siguiente función recupera información relacionada con **glDeleteTextures**:</span><span class="sxs-lookup"><span data-stu-id="4a088-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="4a088-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="4a088-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="4a088-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a088-131">Requirements</span></span>



| <span data-ttu-id="4a088-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a088-132">Requirement</span></span> | <span data-ttu-id="4a088-133">Value</span><span class="sxs-lookup"><span data-stu-id="4a088-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a088-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a088-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4a088-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4a088-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4a088-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a088-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4a088-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a088-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a088-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a088-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a088-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a088-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4a088-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a088-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a088-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a088-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a088-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a088-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a088-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a088-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a088-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a088-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a088-145">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="4a088-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="4a088-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4a088-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4a088-147">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="4a088-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="4a088-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4a088-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4a088-149">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="4a088-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="4a088-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4a088-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4a088-151">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4a088-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="4a088-152">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="4a088-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="4a088-153">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="4a088-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="4a088-154">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="4a088-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="4a088-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="4a088-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="4a088-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="4a088-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="4a088-157">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4a088-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





