---
title: función glGetTexParameteriv (GL. h)
description: Las funciones glGetTexParameterfv y glGetTexParameteriv devuelven los valores de los parámetros de textura. | función glGetTexParameteriv (GL. h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- glGetTexParameteriv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78983594487fd22917c15a5b211c529b6b14d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670195"
---
# <a name="glgettexparameteriv-function"></a><span data-ttu-id="3d161-105">glGetTexParameteriv función)</span><span class="sxs-lookup"><span data-stu-id="3d161-105">glGetTexParameteriv function</span></span>

<span data-ttu-id="3d161-106">Las funciones [**glGetTexParameterfv**](glgettexparameterfv.md) y **glGetTexParameteriv** devuelven los valores de los parámetros de textura.</span><span class="sxs-lookup"><span data-stu-id="3d161-106">The [**glGetTexParameterfv**](glgettexparameterfv.md) and **glGetTexParameteriv** functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d161-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d161-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="3d161-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d161-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d161-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="3d161-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="3d161-110">Nombre simbólico de la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="3d161-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="3d161-111">Se aceptan las texturas GL \_ \_ 1D y GL Texture \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="3d161-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3d161-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="3d161-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3d161-113">Nombre simbólico de un parámetro de textura.</span><span class="sxs-lookup"><span data-stu-id="3d161-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="3d161-114">Se aceptan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="3d161-114">The following values are accepted.</span></span>



| <span data-ttu-id="3d161-115">Value</span><span class="sxs-lookup"><span data-stu-id="3d161-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="3d161-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3d161-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="3d161-117"><dt>**\_filtro de textura de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="3d161-118">Devuelve el filtro de aumento de la textura de un solo valor, una constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="3d161-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="3d161-119"><dt>**\_ \_ filtro mínimo de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="3d161-120">Devuelve el filtro minificación de textura de un solo valor, una constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="3d161-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="3d161-121"><dt>**\_ajuste de textura de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="3d161-122">Devuelve la función de ajuste de un solo valor para las coordenadas de textura *s*, una constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="3d161-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="3d161-123"><dt>**ajuste de textura de GL \_ \_ \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="3d161-124">Devuelve la función de ajuste de un solo valor para la coordenada de textura *t*, una constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="3d161-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="3d161-125"><dt>**\_color de \_ borde de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="3d161-126">Devuelve cuatro números enteros o de punto flotante que conforman el color RGBA del borde de la textura.</span><span class="sxs-lookup"><span data-stu-id="3d161-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="3d161-127">Los valores de punto flotante se devuelven en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="3d161-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="3d161-128">Los valores enteros se devuelven como una asignación lineal de la representación de punto flotante interna, de modo que 1,0 se asigna al entero representable más positivo y-1,0 se asigna al entero representable más negativo.</span><span class="sxs-lookup"><span data-stu-id="3d161-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="3d161-129"><dt>**\_prioridad de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="3d161-130">Devuelve la prioridad de residencia de la textura de destino (o la textura con nombre enlazada a ella).</span><span class="sxs-lookup"><span data-stu-id="3d161-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="3d161-131">El valor inicial es 1.</span><span class="sxs-lookup"><span data-stu-id="3d161-131">The initial value is 1.</span></span> <span data-ttu-id="3d161-132">Vea [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="3d161-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="3d161-133"><dt>**\_residente de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="3d161-134">Devuelve el estado de residencia de la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="3d161-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="3d161-135">Si el valor devuelto en params es GL \_ true, la textura es residente en la memoria de textura.</span><span class="sxs-lookup"><span data-stu-id="3d161-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="3d161-136">Vea [**glAreTexturesResident**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="3d161-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3d161-137">*params*</span><span class="sxs-lookup"><span data-stu-id="3d161-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3d161-138">Devuelve los parámetros de textura.</span><span class="sxs-lookup"><span data-stu-id="3d161-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d161-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d161-139">Return value</span></span>

<span data-ttu-id="3d161-140">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d161-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d161-141">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3d161-141">Error codes</span></span>

<span data-ttu-id="3d161-142">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="3d161-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3d161-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d161-143">Name</span></span>                                                                                                  | <span data-ttu-id="3d161-144">Significado</span><span class="sxs-lookup"><span data-stu-id="3d161-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d161-145"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3d161-146">el *destino* o *el nombre* no eran un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="3d161-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="3d161-147"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3d161-148">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3d161-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3d161-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d161-149">Remarks</span></span>

<span data-ttu-id="3d161-150">La función **glGetTexParameter** devuelve en *params* el valor o los valores del parámetro Texture especificado como *PName*.</span><span class="sxs-lookup"><span data-stu-id="3d161-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="3d161-151">El parámetro de *destino* define la textura de destino, ya sea la textura de GL \_ \_ 1D o la \_ textura \_ de GL 2D, para especificar una texturización unidimensional o bidimensional.</span><span class="sxs-lookup"><span data-stu-id="3d161-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="3d161-152">El parámetro *PName* acepta los mismos símbolos que [**glTexParameter**](gltexparameter-functions.md), con las mismas interpretaciones.</span><span class="sxs-lookup"><span data-stu-id="3d161-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="3d161-153">Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.</span><span class="sxs-lookup"><span data-stu-id="3d161-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d161-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d161-154">Requirements</span></span>



| <span data-ttu-id="3d161-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d161-155">Requirement</span></span> | <span data-ttu-id="3d161-156">Value</span><span class="sxs-lookup"><span data-stu-id="3d161-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d161-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d161-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3d161-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3d161-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d161-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d161-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3d161-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d161-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d161-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d161-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d161-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3d161-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d161-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d161-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d161-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d161-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d161-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d161-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d161-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d161-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d161-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3d161-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3d161-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3d161-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3d161-170">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3d161-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





