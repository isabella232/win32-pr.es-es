---
title: función glColorMaterial (GL. h)
description: La función glColorMaterial hace que un color material realice un seguimiento del color actual.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial (función) OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422395"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="81db7-104">glColorMaterial función)</span><span class="sxs-lookup"><span data-stu-id="81db7-104">glColorMaterial function</span></span>

<span data-ttu-id="81db7-105">La función **glColorMaterial** hace que un color material realice un seguimiento del color actual.</span><span class="sxs-lookup"><span data-stu-id="81db7-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="81db7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81db7-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="81db7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81db7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81db7-108">*Portada*</span><span class="sxs-lookup"><span data-stu-id="81db7-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="81db7-109">Especifica si los parámetros de material delantero, trasero o ambos deben realizar un seguimiento del color actual.</span><span class="sxs-lookup"><span data-stu-id="81db7-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="81db7-110">Los valores aceptados son el \_ front-end de contab \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="81db7-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="81db7-111">El valor predeterminado es GL \_ Front \_ y \_ back.</span><span class="sxs-lookup"><span data-stu-id="81db7-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="81db7-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="81db7-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="81db7-113">Especifica cuál de los diversos parámetros de material realiza un seguimiento del color actual.</span><span class="sxs-lookup"><span data-stu-id="81db7-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="81db7-114">Los valores aceptados son \_ emisión de contabilidad, ambiente de contabilidad general \_ , difusión de contab \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="81db7-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="81db7-115">El valor predeterminado es \_ ambiente \_ de contabilidad y \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="81db7-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81db7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81db7-116">Return value</span></span>

<span data-ttu-id="81db7-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="81db7-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81db7-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="81db7-118">Error codes</span></span>

<span data-ttu-id="81db7-119">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="81db7-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="81db7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="81db7-120">Name</span></span>                                                                                                  | <span data-ttu-id="81db7-121">Significado</span><span class="sxs-lookup"><span data-stu-id="81db7-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81db7-122"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81db7-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="81db7-123">la *esfera* o el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="81db7-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="81db7-124"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81db7-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81db7-125">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="81db7-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81db7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81db7-126">Remarks</span></span>

<span data-ttu-id="81db7-127">La función **glColorMaterial** especifica qué parámetros de material hacen un seguimiento del color actual.</span><span class="sxs-lookup"><span data-stu-id="81db7-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="81db7-128">Cuando se habilita \_ el material de color GL \_ , para cada uno de los materiales especificados por la *esfera*, el parámetro de material o los parámetros especificados por el *modo* realizan el seguimiento del color actual en todo momento.</span><span class="sxs-lookup"><span data-stu-id="81db7-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="81db7-129">Habilitar y deshabilitar \_ \_ el material de color de GL con las funciones [**glEnable**](glenable.md) y [**glDisable**](gldisable.md), que se llama con el material de \_ color GL \_ como su argumento.</span><span class="sxs-lookup"><span data-stu-id="81db7-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="81db7-130">De forma predeterminada, el \_ material de color GL \_ está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="81db7-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="81db7-131">Con **glColorMaterial**, puede cambiar un subconjunto de parámetros de material para cada vértice usando solo la función [**glColor**](glcolor-functions.md) , sin llamar a [**glMaterial**](glmaterial-functions.md).</span><span class="sxs-lookup"><span data-stu-id="81db7-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="81db7-132">Si va a especificar solo este tipo de subconjunto de parámetros para cada vértice, es mejor hacerlo con **glColorMaterial** que con **glMaterial**.</span><span class="sxs-lookup"><span data-stu-id="81db7-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="81db7-133">Las siguientes funciones recuperan información relacionada con **glColorMaterial**:</span><span class="sxs-lookup"><span data-stu-id="81db7-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="81db7-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ parámetro de \_ material de color GL de argument \_</span><span class="sxs-lookup"><span data-stu-id="81db7-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="81db7-135">**glGet** con el argumento del \_ material de color de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="81db7-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="81db7-136">[**glIsEnabled**](glisenabled.md) con el argumento \_ material de color GL \_</span><span class="sxs-lookup"><span data-stu-id="81db7-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="81db7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81db7-137">Requirements</span></span>



| <span data-ttu-id="81db7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="81db7-138">Requirement</span></span> | <span data-ttu-id="81db7-139">Value</span><span class="sxs-lookup"><span data-stu-id="81db7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81db7-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81db7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="81db7-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81db7-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81db7-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81db7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="81db7-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81db7-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81db7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81db7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="81db7-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="81db7-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="81db7-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81db7-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="81db7-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81db7-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="81db7-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81db7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81db7-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81db7-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81db7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="81db7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81db7-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="81db7-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="81db7-152">**glColor**</span><span class="sxs-lookup"><span data-stu-id="81db7-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="81db7-153">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="81db7-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="81db7-154">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="81db7-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="81db7-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="81db7-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="81db7-156">**glGet**</span><span class="sxs-lookup"><span data-stu-id="81db7-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="81db7-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="81db7-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="81db7-158">**glLight**</span><span class="sxs-lookup"><span data-stu-id="81db7-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="81db7-159">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="81db7-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="81db7-160">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="81db7-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





