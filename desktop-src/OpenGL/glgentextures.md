---
title: función glGenTextures (GL. h)
description: La función glGenTextures genera nombres de textura.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures (función) OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997004"
---
# <a name="glgentextures-function"></a><span data-ttu-id="3c454-104">glGenTextures función)</span><span class="sxs-lookup"><span data-stu-id="3c454-104">glGenTextures function</span></span>

<span data-ttu-id="3c454-105">La función **glGenTextures** genera nombres de textura.</span><span class="sxs-lookup"><span data-stu-id="3c454-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c454-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c454-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="3c454-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c454-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c454-108">*n*</span><span class="sxs-lookup"><span data-stu-id="3c454-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="3c454-109">El número de nombres de textura que se van a generar.</span><span class="sxs-lookup"><span data-stu-id="3c454-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="3c454-110">*texturas*</span><span class="sxs-lookup"><span data-stu-id="3c454-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="3c454-111">Puntero al primer elemento de una matriz en la que se almacenan los nombres de textura generados.</span><span class="sxs-lookup"><span data-stu-id="3c454-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c454-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c454-112">Return value</span></span>

<span data-ttu-id="3c454-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3c454-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c454-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3c454-114">Error codes</span></span>

<span data-ttu-id="3c454-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="3c454-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3c454-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c454-116">Name</span></span>                                                                                                  | <span data-ttu-id="3c454-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3c454-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c454-118"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c454-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="3c454-119">*n* era un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="3c454-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3c454-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c454-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3c454-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3c454-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c454-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c454-122">Remarks</span></span>

<span data-ttu-id="3c454-123">La función **glGenTextures** devuelve *n* nombres de textura en el parámetro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="3c454-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="3c454-124">Los nombres de las texturas no son necesariamente un conjunto contiguo de enteros; sin embargo, ninguno de los nombres devueltos se puede haber estado usando inmediatamente antes de llamar a la función **glGenTextures** .</span><span class="sxs-lookup"><span data-stu-id="3c454-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="3c454-125">Las texturas generadas suponen la dimensionalidad del destino de textura al que se enlazan por primera vez con la función [**glBindTexture**](glbindtexture.md) .</span><span class="sxs-lookup"><span data-stu-id="3c454-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="3c454-126">Los nombres de textura devueltos por **glGenTextures** no se devuelven en las llamadas subsiguientes a **glGenTextures** , a menos que se eliminen primero llamando a [**glDeleteTextures**](gldeletetextures.md).</span><span class="sxs-lookup"><span data-stu-id="3c454-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="3c454-127">No se puede incluir **glGenTextures** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="3c454-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="3c454-128">La función **glGenTextures** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3c454-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="3c454-129">La siguiente función recupera información relacionada con **glGenTextures**:</span><span class="sxs-lookup"><span data-stu-id="3c454-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="3c454-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="3c454-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="3c454-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c454-131">Requirements</span></span>



| <span data-ttu-id="3c454-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c454-132">Requirement</span></span> | <span data-ttu-id="3c454-133">Value</span><span class="sxs-lookup"><span data-stu-id="3c454-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c454-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c454-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3c454-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3c454-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c454-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c454-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3c454-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c454-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c454-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c454-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c454-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c454-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3c454-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c454-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c454-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c454-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c454-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c454-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c454-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c454-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c454-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c454-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c454-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3c454-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3c454-146">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="3c454-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="3c454-147">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="3c454-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="3c454-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3c454-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3c454-149">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3c454-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3c454-150">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3c454-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="3c454-151">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="3c454-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="3c454-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="3c454-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="3c454-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="3c454-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="3c454-154">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3c454-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





