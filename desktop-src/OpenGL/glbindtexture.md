---
title: función glBindTexture (GL. h)
description: La función glBindTexture permite la creación de una textura con nombre que está enlazada a un destino de textura.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture (función) OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422398"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="eb7a1-104">glBindTexture función)</span><span class="sxs-lookup"><span data-stu-id="eb7a1-104">glBindTexture function</span></span>

<span data-ttu-id="eb7a1-105">La función **glBindTexture** permite la creación de una textura con nombre que está enlazada a un destino de textura.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7a1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb7a1-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="eb7a1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb7a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7a1-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="eb7a1-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7a1-109">Destino al que está enlazada la textura.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-109">The target to which the texture is bound.</span></span> <span data-ttu-id="eb7a1-110">Debe tener el valor de GL \_ Texture \_ 1D o la textura de GL \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="eb7a1-111">*degrada*</span><span class="sxs-lookup"><span data-stu-id="eb7a1-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7a1-112">Nombre de una textura; el nombre de la textura no puede estar actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb7a1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb7a1-113">Return value</span></span>

<span data-ttu-id="eb7a1-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb7a1-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="eb7a1-115">Error codes</span></span>

<span data-ttu-id="eb7a1-116">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="eb7a1-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb7a1-117">Name</span></span>                                                                                                  | <span data-ttu-id="eb7a1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="eb7a1-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb7a1-119"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb7a1-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="eb7a1-120">El *destino* del parámetro no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="eb7a1-121"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb7a1-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="eb7a1-122">La *textura* del parámetro no tenía la misma dimensionalidad que el *destino* o se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="eb7a1-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eb7a1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb7a1-123">Remarks</span></span>

<span data-ttu-id="eb7a1-124">La función **glBindTexture** permite crear una textura con nombre.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="eb7a1-125">La llamada a **glBindTexture** con el *destino* establecido en GL \_ Texture \_ 1D o la textura GL \_ \_ 2D y la *textura* establecida en el nombre de la nueva textura que ha creado enlaza el nombre de textura al destino de textura adecuado.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="eb7a1-126">Cuando una textura se enlaza a un destino, el enlace anterior para ese destino deja de estar en vigor.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="eb7a1-127">Los nombres de textura son enteros sin signo con el valor cero reservado para representar la textura predeterminada para cada destino de textura.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="eb7a1-128">Los nombres de textura y el contenido de textura correspondiente son locales para el espacio de lista de presentación compartido del contexto de representación de OpenGL actual. dos contextos de representación comparten nombres de textura solo si también comparten listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="eb7a1-129">Puede generar un conjunto de nuevos nombres de textura mediante [**glGenTextures**](glgentextures.md).</span><span class="sxs-lookup"><span data-stu-id="eb7a1-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="eb7a1-130">Cuando una textura se enlaza por primera vez, se asume la dimensionalidad de su destino de textura. una textura enlazada a una textura de GL \_ \_ 1D se convierte en unidimensional y una textura enlazada a la textura de GL \_ \_ 2D se convierte en bidimensional.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="eb7a1-131">Las operaciones que se realizan en un destino de textura también afectan a una textura enlazada al destino.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="eb7a1-132">Cuando se consulta un destino de textura, el valor devuelto es el estado de la textura enlazada a él.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="eb7a1-133">Los destinos de texturas se convierten en alias para las texturas actualmente enlazadas a ellos.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="eb7a1-134">Al enlazar una textura con **glBindTexture**, el enlace permanece activo hasta que se enlaza una textura diferente al mismo destino o se elimina la textura enlazada con la función [**glDeleteTextures**](gldeletetextures.md) .</span><span class="sxs-lookup"><span data-stu-id="eb7a1-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="eb7a1-135">Una vez que cree una textura con nombre, puede enlazarla a un destino de textura que tenga la misma dimensionalidad que la frecuencia que necesite.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="eb7a1-136">Normalmente, es mucho más rápido usar **glBindTexture** para enlazar una textura con nombre existente a uno de los destinos de textura que para volver a cargar la imagen de textura mediante [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="eb7a1-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="eb7a1-137">Para obtener más control sobre el rendimiento de la texturización, use [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="eb7a1-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="eb7a1-138">Puede incluir llamadas a **glBindTexture** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="eb7a1-139">La función **glBindTexture** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="eb7a1-140">Las siguientes funciones recuperan información relacionada con **glBindTexture**:</span><span class="sxs-lookup"><span data-stu-id="eb7a1-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="eb7a1-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con enlace de la \_ textura \_ 1D de \_ argumento</span><span class="sxs-lookup"><span data-stu-id="eb7a1-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="eb7a1-142">**glGet** con el argumento \_ de \_ bidimensional textura 2D \_ enlace</span><span class="sxs-lookup"><span data-stu-id="eb7a1-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="eb7a1-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb7a1-143">Requirements</span></span>



| <span data-ttu-id="eb7a1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb7a1-144">Requirement</span></span> | <span data-ttu-id="eb7a1-145">Value</span><span class="sxs-lookup"><span data-stu-id="eb7a1-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7a1-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb7a1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="eb7a1-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eb7a1-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eb7a1-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb7a1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="eb7a1-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb7a1-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb7a1-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb7a1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb7a1-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb7a1-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="eb7a1-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb7a1-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb7a1-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb7a1-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eb7a1-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb7a1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb7a1-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb7a1-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb7a1-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb7a1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7a1-157">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-158">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-159">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-160">**glGet**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-162">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-163">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="eb7a1-166">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





