---
title: función glGetTexGenfv (GL. h)
description: Las funciones glGetTexGendv, glGetTexGenfv y glGetTexGeniv devuelven parámetros de generación de coordenadas de textura. | función glGetTexGenfv (GL. h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- glGetTexGenfv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e527d0388b8aca7239ba1c51dccdce15de3cd8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362169"
---
# <a name="glgettexgenfv-function"></a><span data-ttu-id="f99cb-105">glGetTexGenfv función)</span><span class="sxs-lookup"><span data-stu-id="f99cb-105">glGetTexGenfv function</span></span>

<span data-ttu-id="f99cb-106">Las funciones [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv** y [**glGetTexGeniv**](glgettexgeniv.md) devuelven parámetros de generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f99cb-106">The [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv**, and [**glGetTexGeniv**](glgettexgeniv.md) functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99cb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f99cb-107">Syntax</span></span>


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="f99cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f99cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99cb-109">*coords*</span><span class="sxs-lookup"><span data-stu-id="f99cb-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="f99cb-110">Coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="f99cb-110">A texture coordinate.</span></span> <span data-ttu-id="f99cb-111">Debe ser GL \_ S, GL \_ T, GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="f99cb-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="f99cb-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="f99cb-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="f99cb-113">Nombre simbólico de los valores que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="f99cb-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="f99cb-114">Debe ser el modo de generación de \_ textura GL \_ \_ o el nombre de una de las ecuaciones del plano de generación de textura: plano de \_ objeto GL \_ o plano de ojo de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f99cb-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="f99cb-115">Estos valores son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f99cb-115">These values are as follows.</span></span>



| <span data-ttu-id="f99cb-116">Value</span><span class="sxs-lookup"><span data-stu-id="f99cb-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="f99cb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f99cb-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="f99cb-118"><dt>**\_modo de generación de texturas GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="f99cb-119">El parámetro *params* devuelve la función de generación de textura de un solo valor, una constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="f99cb-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="f99cb-120"><dt>**\_plano del objeto GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="f99cb-121">El parámetro *params* devuelve los cuatro coeficientes de ecuaciones de plano que especifican la generación de coordenada lineal del objeto.</span><span class="sxs-lookup"><span data-stu-id="f99cb-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="f99cb-122">Los valores enteros, cuando se solicitan, se asignan directamente desde la representación interna de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f99cb-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="f99cb-123"><dt>**\_plano de ojo de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="f99cb-124">El parámetro *params* devuelve los cuatro coeficientes de ecuaciones de plano que especifican la generación de coordenada lineal.</span><span class="sxs-lookup"><span data-stu-id="f99cb-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="f99cb-125">Los valores enteros, cuando se solicitan, se asignan directamente desde la representación interna de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f99cb-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="f99cb-126">Los valores devueltos son los que se mantienen en coordenadas oculares.</span><span class="sxs-lookup"><span data-stu-id="f99cb-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="f99cb-127">No son iguales a los valores especificados mediante [**glTexGen**](gltexgen-functions.md), a menos que se haya identificado la matriz MODELVIEW en el momento en que se llamó a **glTexGen** .</span><span class="sxs-lookup"><span data-stu-id="f99cb-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f99cb-128">*params*</span><span class="sxs-lookup"><span data-stu-id="f99cb-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="f99cb-129">Devuelve los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="f99cb-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f99cb-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f99cb-130">Return value</span></span>

<span data-ttu-id="f99cb-131">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f99cb-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f99cb-132">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f99cb-132">Error codes</span></span>

<span data-ttu-id="f99cb-133">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="f99cb-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f99cb-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="f99cb-134">Name</span></span>                                                                                                  | <span data-ttu-id="f99cb-135">Significado</span><span class="sxs-lookup"><span data-stu-id="f99cb-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f99cb-136"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f99cb-137">la expresión de *coordenadas* o *PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="f99cb-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="f99cb-138"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f99cb-139">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f99cb-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f99cb-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f99cb-140">Remarks</span></span>

<span data-ttu-id="f99cb-141">La función **glGetTexGen** devuelve en *params* parámetros seleccionados de una función de generación de coordenadas de textura que especificó con **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="f99cb-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="f99cb-142">El parámetro *coords* asigna un nombre a una de las coordenadas de textura (*s*, *t*, *r*, *q*), mediante la constante simbólica GL \_ s, GL \_ t, GL \_ r o GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="f99cb-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="f99cb-143">Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.</span><span class="sxs-lookup"><span data-stu-id="f99cb-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f99cb-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f99cb-144">Requirements</span></span>



| <span data-ttu-id="f99cb-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f99cb-145">Requirement</span></span> | <span data-ttu-id="f99cb-146">Value</span><span class="sxs-lookup"><span data-stu-id="f99cb-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f99cb-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f99cb-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f99cb-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f99cb-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f99cb-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f99cb-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f99cb-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f99cb-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f99cb-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f99cb-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f99cb-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f99cb-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f99cb-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f99cb-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f99cb-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f99cb-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f99cb-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f99cb-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f99cb-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="f99cb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99cb-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f99cb-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f99cb-159">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f99cb-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f99cb-160">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="f99cb-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





