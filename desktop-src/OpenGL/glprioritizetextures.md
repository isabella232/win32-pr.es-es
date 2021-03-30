---
title: función glPrioritizeTextures (GL. h)
description: La función glPrioritizeTextures establece la prioridad de residencia de las texturas.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glPrioritizeTextures (función) OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801634"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="e9cfc-104">glPrioritizeTextures función)</span><span class="sxs-lookup"><span data-stu-id="e9cfc-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="e9cfc-105">La función **glPrioritizeTextures** establece la prioridad de residencia de las texturas.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9cfc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9cfc-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="e9cfc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9cfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cfc-108">*n*</span><span class="sxs-lookup"><span data-stu-id="e9cfc-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cfc-109">Número de texturas que se van a clasificar por orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="e9cfc-110">*texturas*</span><span class="sxs-lookup"><span data-stu-id="e9cfc-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cfc-111">Puntero al primer elemento de una matriz que contiene los nombres de las texturas que se van a priorizar.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="e9cfc-112">*fija*</span><span class="sxs-lookup"><span data-stu-id="e9cfc-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cfc-113">Puntero al primer elemento de una matriz que contiene las prioridades de textura.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="e9cfc-114">Una prioridad especificada en un elemento del parámetro de *prioridades* se aplica a la textura denominada por el elemento correspondiente del parámetro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="e9cfc-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cfc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9cfc-115">Return value</span></span>

<span data-ttu-id="e9cfc-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9cfc-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e9cfc-117">Error codes</span></span>

<span data-ttu-id="e9cfc-118">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e9cfc-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9cfc-119">Name</span></span>                                                                                                  | <span data-ttu-id="e9cfc-120">Significado</span><span class="sxs-lookup"><span data-stu-id="e9cfc-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9cfc-121"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cfc-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e9cfc-122">*n* era un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="e9cfc-123"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cfc-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e9cfc-124">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e9cfc-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9cfc-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9cfc-125">Remarks</span></span>

<span data-ttu-id="e9cfc-126">La función **glPrioritizeTextures** asigna las *n* prioridades de textura especificadas en el parámetro de *prioridades* a las *n* texturas mencionadas en el parámetro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="e9cfc-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="e9cfc-127">En los equipos con una cantidad limitada de memoria de textura, OpenGL establece un "conjunto de trabajo" de texturas que residen en la memoria de textura.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="e9cfc-128">Estas texturas se pueden enlazar a un destino de textura mucho más eficaz que las texturas que no son residentes.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="e9cfc-129">Al especificar una prioridad para cada textura, la función **glPrioritizeTextures** le permite determinar qué texturas deben ser residentes.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="e9cfc-130">Los elementos de prioridades de textura en las *prioridades* se fijan al intervalo \[ 0,0, 1,0 \] antes de que se asignen.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="e9cfc-131">Cero indica la prioridad más baja; por lo tanto, es menos probable que las texturas con prioridad cero sean residentes.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="e9cfc-132">El valor 1,0 indica la prioridad máxima; por lo tanto, es más probable que las texturas con prioridad 1,0 sean residentes.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="e9cfc-133">Sin embargo, no se garantiza que las texturas sean residentes hasta que se enlazan.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="e9cfc-134">La función **glPrioritizeTextures** omite los intentos de dar prioridad a la textura 0 o cualquier nombre de textura que no corresponda a una textura existente.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="e9cfc-135">Ninguna de las funciones nombradas por el parámetro *Textures* debe estar enlazada a un destino de textura.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="e9cfc-136">Si una textura está actualmente enlazada, también puede usar la función [**glTexParameter**](gltexparameter-functions.md) para establecer su prioridad.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="e9cfc-137">Esta es la única manera de establecer la prioridad de una textura predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="e9cfc-138">Puede incluir **glPrioritizeTextures** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="e9cfc-139">La siguiente función recupera la prioridad de una textura enlazada actualmente relacionada con **glPrioritizeTextures**:</span><span class="sxs-lookup"><span data-stu-id="e9cfc-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="e9cfc-140">[**glGetTexParameter**](glgettexparameter.md) con el nombre de parámetro \_ prioridad de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="e9cfc-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="e9cfc-141">La función **glPrioritizeTextures** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e9cfc-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9cfc-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9cfc-142">Requirements</span></span>



| <span data-ttu-id="e9cfc-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9cfc-143">Requirement</span></span> | <span data-ttu-id="e9cfc-144">Value</span><span class="sxs-lookup"><span data-stu-id="e9cfc-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cfc-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9cfc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cfc-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e9cfc-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e9cfc-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9cfc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cfc-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9cfc-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9cfc-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9cfc-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9cfc-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9cfc-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e9cfc-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9cfc-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9cfc-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9cfc-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9cfc-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9cfc-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9cfc-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9cfc-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cfc-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9cfc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cfc-156">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="e9cfc-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e9cfc-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e9cfc-159">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="e9cfc-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="e9cfc-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="e9cfc-162">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="e9cfc-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





