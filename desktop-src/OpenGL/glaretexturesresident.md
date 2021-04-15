---
title: función glAreTexturesResident (GL. h)
description: La función glAreTexturesResident determina si los objetos de textura especificados están residentes en la memoria de textura.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident (función) OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676787"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="23b1c-104">glAreTexturesResident función)</span><span class="sxs-lookup"><span data-stu-id="23b1c-104">glAreTexturesResident function</span></span>

<span data-ttu-id="23b1c-105">La función **glAreTexturesResident** determina si los objetos de textura especificados están residentes en la memoria de textura.</span><span class="sxs-lookup"><span data-stu-id="23b1c-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b1c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23b1c-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="23b1c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23b1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b1c-108">*n*</span><span class="sxs-lookup"><span data-stu-id="23b1c-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="23b1c-109">Número de texturas que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="23b1c-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="23b1c-110">*texturas*</span><span class="sxs-lookup"><span data-stu-id="23b1c-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="23b1c-111">Dirección de una matriz que contiene los nombres de las texturas que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="23b1c-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="23b1c-112">*residencias*</span><span class="sxs-lookup"><span data-stu-id="23b1c-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="23b1c-113">Dirección de una matriz en la que se devuelve el estado de residencia de la textura.</span><span class="sxs-lookup"><span data-stu-id="23b1c-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="23b1c-114">El estado de residencia de una textura denominada por un elemento de *texturas* se devuelve en el elemento de *residencias* correspondiente.</span><span class="sxs-lookup"><span data-stu-id="23b1c-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="23b1c-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="23b1c-115">Error codes</span></span>

<span data-ttu-id="23b1c-116">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="23b1c-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="23b1c-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="23b1c-117">Name</span></span>                                                                                                  | <span data-ttu-id="23b1c-118">Significado</span><span class="sxs-lookup"><span data-stu-id="23b1c-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23b1c-119"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23b1c-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="23b1c-120">*n* era un valor negativo, un elemento en las *texturas* era cero o un elemento de las *texturas* no contenía un identificador de textura.</span><span class="sxs-lookup"><span data-stu-id="23b1c-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="23b1c-121"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23b1c-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="23b1c-122">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="23b1c-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="23b1c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23b1c-123">Remarks</span></span>

<span data-ttu-id="23b1c-124">En los equipos con una cantidad limitada de memoria de textura, OpenGL establece un conjunto de trabajo de texturas que residen en la memoria de textura.</span><span class="sxs-lookup"><span data-stu-id="23b1c-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="23b1c-125">Estas texturas se pueden enlazar a un destino de textura mucho más eficaz que las texturas que no son residentes.</span><span class="sxs-lookup"><span data-stu-id="23b1c-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="23b1c-126">La función **glAreTexturesResident** consulta el estado de residencia de la textura de las *n* texturas nombradas por los elementos de las *texturas*.</span><span class="sxs-lookup"><span data-stu-id="23b1c-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="23b1c-127">Si todas las texturas con nombre son residentes, **glAreTexturesResident** devuelve GL \_ true y el contenido de *residencias* no se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="23b1c-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="23b1c-128">Si alguna de las texturas con nombre no es residente, **glAreTexturesResident** devuelve GL \_ false y se devuelve el estado detallado en los *n* elementos de *residencias*.</span><span class="sxs-lookup"><span data-stu-id="23b1c-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="23b1c-129">Si un elemento de *residencias* es un \_ valor de GL, la textura denominada por el elemento de *texturas* correspondiente se encuentra residente en la memoria de textura.</span><span class="sxs-lookup"><span data-stu-id="23b1c-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="23b1c-130">Para consultar el estado de residencia de una sola textura enlazada, llame a [**glGetTexParameter**](glgettexparameter.md) con el parámetro de *destino* establecido en la textura de destino a la que está enlazado el destino y establezca el parámetro *PName* en residente de textura de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="23b1c-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="23b1c-131">Debe utilizar este método para consultar el estado residente de una textura predeterminada.</span><span class="sxs-lookup"><span data-stu-id="23b1c-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="23b1c-132">No se puede incluir **glAreTexturesResident** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="23b1c-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="23b1c-133">La función **glAreTexturesResident** devuelve el estado de residencia de las texturas en el momento de la invocación.</span><span class="sxs-lookup"><span data-stu-id="23b1c-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="23b1c-134">No garantiza que las texturas seguirán siendo residentes en cualquier otro momento.</span><span class="sxs-lookup"><span data-stu-id="23b1c-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="23b1c-135">Si las texturas residen en la memoria virtual (no hay memoria de textura), se consideran siempre residentes.</span><span class="sxs-lookup"><span data-stu-id="23b1c-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="23b1c-136">La función **glAreTexturesResident** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="23b1c-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23b1c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b1c-137">Requirements</span></span>



| <span data-ttu-id="23b1c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b1c-138">Requirement</span></span> | <span data-ttu-id="23b1c-139">Value</span><span class="sxs-lookup"><span data-stu-id="23b1c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23b1c-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23b1c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="23b1c-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23b1c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="23b1c-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23b1c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="23b1c-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23b1c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23b1c-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23b1c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b1c-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="23b1c-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="23b1c-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23b1c-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="23b1c-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23b1c-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23b1c-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23b1c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b1c-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b1c-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b1c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="23b1c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b1c-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="23b1c-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="23b1c-152">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="23b1c-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="23b1c-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="23b1c-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="23b1c-154">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="23b1c-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="23b1c-155">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="23b1c-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="23b1c-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="23b1c-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="23b1c-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="23b1c-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





