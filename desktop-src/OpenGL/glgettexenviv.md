---
title: función glGetTexEnviv (GL. h)
description: Las funciones glGetTexEnvfv y glGetTexEnviv devuelven parámetros de entorno de textura. | función glGetTexEnviv (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- glGetTexEnviv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670143"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="a16aa-105">glGetTexEnviv función)</span><span class="sxs-lookup"><span data-stu-id="a16aa-105">glGetTexEnviv function</span></span>

<span data-ttu-id="a16aa-106">Las funciones [**glGetTexEnvfv**](glgettexenvfv.md) y **glGetTexEnviv** devuelven parámetros de entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="a16aa-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16aa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a16aa-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="a16aa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a16aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a16aa-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="a16aa-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a16aa-110">Entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="a16aa-110">A texture environment.</span></span> <span data-ttu-id="a16aa-111">Debe ser un \_ \_ env Texture.</span><span class="sxs-lookup"><span data-stu-id="a16aa-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="a16aa-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="a16aa-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a16aa-113">Nombre simbólico de un parámetro de entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="a16aa-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="a16aa-114">Se aceptan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="a16aa-114">The following values are accepted.</span></span>



| <span data-ttu-id="a16aa-115">Value</span><span class="sxs-lookup"><span data-stu-id="a16aa-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="a16aa-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a16aa-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="a16aa-117"><dt>**\_modo de textura del libro de contabilidad \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="a16aa-118">El parámetro *params* devuelve el modo de entorno de textura de un solo valor, una constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="a16aa-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="a16aa-119"><dt>**\_color de textura de libro de contabilidad \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="a16aa-120">El parámetro *params* devuelve cuatro valores enteros o de punto flotante que son el color del entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="a16aa-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="a16aa-121">Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al entero representable más positivo y-1,0 se asigna al entero representable más negativo.</span><span class="sxs-lookup"><span data-stu-id="a16aa-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a16aa-122">*params*</span><span class="sxs-lookup"><span data-stu-id="a16aa-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a16aa-123">Devuelve los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="a16aa-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a16aa-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a16aa-124">Return value</span></span>

<span data-ttu-id="a16aa-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a16aa-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a16aa-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a16aa-126">Error codes</span></span>

<span data-ttu-id="a16aa-127">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a16aa-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a16aa-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="a16aa-128">Name</span></span>                                                                                                  | <span data-ttu-id="a16aa-129">Significado</span><span class="sxs-lookup"><span data-stu-id="a16aa-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a16aa-130"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a16aa-131">el *destino* o *PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="a16aa-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="a16aa-132"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a16aa-133">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a16aa-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a16aa-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a16aa-134">Remarks</span></span>

<span data-ttu-id="a16aa-135">La función **glGetTexEnv** devuelve en *params* valores seleccionados de un entorno de textura que se especificó con [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a16aa-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="a16aa-136">El parámetro de *destino* especifica un entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="a16aa-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="a16aa-137">Actualmente, solo se define y admite un entorno de textura: GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="a16aa-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="a16aa-138">El parámetro *PName* nombra un parámetro de entorno de textura específico.</span><span class="sxs-lookup"><span data-stu-id="a16aa-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="a16aa-139">Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.</span><span class="sxs-lookup"><span data-stu-id="a16aa-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a16aa-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a16aa-140">Requirements</span></span>



| <span data-ttu-id="a16aa-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16aa-141">Requirement</span></span> | <span data-ttu-id="a16aa-142">Value</span><span class="sxs-lookup"><span data-stu-id="a16aa-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a16aa-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a16aa-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a16aa-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a16aa-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a16aa-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a16aa-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a16aa-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a16aa-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a16aa-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a16aa-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a16aa-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a16aa-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a16aa-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="a16aa-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a16aa-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a16aa-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a16aa-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a16aa-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a16aa-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="a16aa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16aa-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a16aa-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a16aa-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a16aa-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a16aa-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="a16aa-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





