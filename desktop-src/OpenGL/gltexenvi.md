---
title: función glTexEnvi (GL. h)
description: La función glTexEnvi establece un parámetro de entorno de textura.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- glTexEnvi (función) OpenGL
topic_type:
- apiref
api_name:
- glTexEnvi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013b0e4805042ed0967e02df83f143d8bcfd991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665919"
---
# <a name="gltexenvi-function"></a><span data-ttu-id="6c925-104">glTexEnvi función)</span><span class="sxs-lookup"><span data-stu-id="6c925-104">glTexEnvi function</span></span>

<span data-ttu-id="6c925-105">La función **glTexEnvi** establece un parámetro de entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="6c925-105">The **glTexEnvi** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c925-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c925-106">Syntax</span></span>


```C++
void WINAPI glTexEnvi(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="6c925-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c925-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c925-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="6c925-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="6c925-109">Entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="6c925-109">A texture environment.</span></span> <span data-ttu-id="6c925-110">Debe ser un \_ \_ env Texture.</span><span class="sxs-lookup"><span data-stu-id="6c925-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="6c925-111">*PName*</span><span class="sxs-lookup"><span data-stu-id="6c925-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="6c925-112">El nombre simbólico de un parámetro de entorno de textura de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="6c925-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="6c925-113">Debe ser el modo de textura de libro de contabilidad \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6c925-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="6c925-114">*param*</span><span class="sxs-lookup"><span data-stu-id="6c925-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="6c925-115">Una sola constante simbólica, una de GL \_ modulada, GL \_ Decal, GL \_ Blend o el reemplazo de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="6c925-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c925-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c925-116">Return value</span></span>

<span data-ttu-id="6c925-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6c925-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c925-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6c925-118">Error codes</span></span>

<span data-ttu-id="6c925-119">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6c925-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6c925-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c925-120">Name</span></span>                                                                                                  | <span data-ttu-id="6c925-121">Significado</span><span class="sxs-lookup"><span data-stu-id="6c925-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c925-122"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6c925-123">el *destino* o *PName* no era uno de los valores definidos aceptados o cuando los *parámetros* deberían tener un valor constante definido (basado en el valor de *PName*) y no lo hacían.</span><span class="sxs-lookup"><span data-stu-id="6c925-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="6c925-124"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6c925-125">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6c925-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="6c925-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c925-126">Remarks</span></span>

<span data-ttu-id="6c925-127">Un entorno de textura especifica cómo se interpretan los valores de textura cuando se textura un fragmento.</span><span class="sxs-lookup"><span data-stu-id="6c925-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="6c925-128">El parámetro de *destino* debe ser de \_ textura GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="6c925-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="6c925-129">El parámetro *PName* es el modo de textura del libro de contabilidad \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6c925-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="6c925-130">Se definen tres funciones de textura: libro de contabilidad general \_ , \_ Decal y GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="6c925-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="6c925-131">Una función de textura actúa en el fragmento que se va a texturar mediante el valor de la imagen de textura que se aplica al fragmento (vea [**glTexParameter**](gltexparameter-functions.md)) y genera un color RGBA para ese fragmento.</span><span class="sxs-lookup"><span data-stu-id="6c925-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="6c925-132">En la tabla siguiente se muestra cómo se genera el color RGBA para cada una de las tres funciones de textura que se pueden elegir.</span><span class="sxs-lookup"><span data-stu-id="6c925-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="6c925-133">*C* es un triple de valores de color (RGB) *y es* el valor alfa asociado.</span><span class="sxs-lookup"><span data-stu-id="6c925-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="6c925-134">Los valores RGBA extraídos de una imagen de textura están en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="6c925-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="6c925-135">El subíndice *f* hace referencia al fragmento entrante, el subíndice *t* a la imagen de textura, el subíndice *c* al color del entorno de textura y el subíndice *v* indica un valor generado por la función de textura.</span><span class="sxs-lookup"><span data-stu-id="6c925-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="6c925-136">Una imagen de textura puede tener hasta cuatro componentes por elemento de textura (vea [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="6c925-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="6c925-137">En una imagen de un componente, lt indica que se trata de un único componente.</span><span class="sxs-lookup"><span data-stu-id="6c925-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="6c925-138">Una imagen de dos componentes usa *L?*</span><span class="sxs-lookup"><span data-stu-id="6c925-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="6c925-139">y *a?*</span><span class="sxs-lookup"><span data-stu-id="6c925-139">and *A?*</span></span> <span data-ttu-id="6c925-140">.</span><span class="sxs-lookup"><span data-stu-id="6c925-140">.</span></span> <span data-ttu-id="6c925-141">Una imagen de tres componentes solo tiene un valor de color, *C?*</span><span class="sxs-lookup"><span data-stu-id="6c925-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="6c925-142">.</span><span class="sxs-lookup"><span data-stu-id="6c925-142">.</span></span> <span data-ttu-id="6c925-143">Una imagen de cuatro componentes tiene un valor de color *C?*</span><span class="sxs-lookup"><span data-stu-id="6c925-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="6c925-144">y un valor alfa *a?*</span><span class="sxs-lookup"><span data-stu-id="6c925-144">and an alpha value *A?*</span></span> <span data-ttu-id="6c925-145">.</span><span class="sxs-lookup"><span data-stu-id="6c925-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6c925-146">Número de componentes</span><span class="sxs-lookup"><span data-stu-id="6c925-146">Number of components</span></span></th>
<th><span data-ttu-id="6c925-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="6c925-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="6c925-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="6c925-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="6c925-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="6c925-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="6c925-150">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="6c925-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6c925-151"><em>C<sub>v</sub> </em>  =  <em>¿L?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="6c925-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="6c925-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="6c925-153">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="6c925-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6c925-154"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-154"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="6c925-155"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="6c925-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="6c925-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c925-157"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="6c925-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="6c925-158"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="6c925-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="6c925-159">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="6c925-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6c925-160"><em>C<sub>v</sub> </em>  =  <em>¿L?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="6c925-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="6c925-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="6c925-162">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="6c925-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6c925-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="6c925-164"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="6c925-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="6c925-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c925-166"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="6c925-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="6c925-167"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="6c925-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="6c925-168">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="6c925-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6c925-169"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="6c925-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="6c925-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="6c925-171"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="6c925-172">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="6c925-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c925-173"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="6c925-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="6c925-174"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="6c925-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="6c925-175">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="6c925-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6c925-176"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="6c925-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="6c925-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="6c925-178"><em>C<sub>v</sub> </em> = (1- <em>a?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="6c925-179"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="6c925-180"><em>Unidad?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="6c925-181">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="6c925-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c925-182"><em>A<sub>v</sub> </em>  =  <em>R?</em></span><span class="sxs-lookup"><span data-stu-id="6c925-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="6c925-183"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="6c925-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="6c925-184"><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="6c925-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="6c925-185">\_De forma predeterminada, la textura de GL del \_ \_ modo env es el \_ modular GL.</span><span class="sxs-lookup"><span data-stu-id="6c925-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="6c925-186">La siguiente función recupera información relacionada con **glTexEnvi**:</span><span class="sxs-lookup"><span data-stu-id="6c925-186">The following function retrieves information related to **glTexEnvi**:</span></span>

[<span data-ttu-id="6c925-187">**glTexGetEnviv**</span><span class="sxs-lookup"><span data-stu-id="6c925-187">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="6c925-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c925-188">Requirements</span></span>



| <span data-ttu-id="6c925-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c925-189">Requirement</span></span> | <span data-ttu-id="6c925-190">Value</span><span class="sxs-lookup"><span data-stu-id="6c925-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c925-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c925-191">Minimum supported client</span></span><br/> | <span data-ttu-id="6c925-192">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c925-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c925-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c925-193">Minimum supported server</span></span><br/> | <span data-ttu-id="6c925-194">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c925-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c925-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c925-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c925-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6c925-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c925-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c925-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c925-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c925-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c925-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c925-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c925-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c925-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6c925-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6c925-203">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6c925-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6c925-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="6c925-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="6c925-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="6c925-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="6c925-206">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6c925-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





