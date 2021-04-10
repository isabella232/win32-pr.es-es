---
title: función glTexEnviv (GL. h)
description: La función glTexEnviv establece un parámetro de entorno de textura.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- glTexEnviv (función) OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905652"
---
# <a name="gltexenviv-function"></a><span data-ttu-id="fad04-104">glTexEnviv función)</span><span class="sxs-lookup"><span data-stu-id="fad04-104">glTexEnviv function</span></span>

<span data-ttu-id="fad04-105">La función **glTexEnviv** establece un parámetro de entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="fad04-105">The **glTexEnviv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad04-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fad04-106">Syntax</span></span>


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="fad04-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fad04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad04-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="fad04-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fad04-109">Entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="fad04-109">A texture environment.</span></span> <span data-ttu-id="fad04-110">Debe ser un \_ \_ env Texture.</span><span class="sxs-lookup"><span data-stu-id="fad04-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="fad04-111">*PName*</span><span class="sxs-lookup"><span data-stu-id="fad04-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fad04-112">El nombre simbólico de un parámetro de entorno de textura de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="fad04-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="fad04-113">Los valores aceptados son el \_ \_ \_ modo de textura de libro de contabilidad y el \_ color env de textura de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fad04-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="fad04-114">*params*</span><span class="sxs-lookup"><span data-stu-id="fad04-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fad04-115">Puntero a una matriz de parámetros: una constante simbólica única o un color RGBA.</span><span class="sxs-lookup"><span data-stu-id="fad04-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad04-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fad04-116">Return value</span></span>

<span data-ttu-id="fad04-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fad04-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fad04-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fad04-118">Error codes</span></span>

<span data-ttu-id="fad04-119">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="fad04-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fad04-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fad04-120">Name</span></span>                                                                                                  | <span data-ttu-id="fad04-121">Significado</span><span class="sxs-lookup"><span data-stu-id="fad04-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fad04-122"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fad04-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fad04-123">el *destino* o *PName* no era uno de los valores definidos aceptados o cuando los *parámetros* deberían tener un valor constante definido (basado en el valor de *PName*) y no lo hacían.</span><span class="sxs-lookup"><span data-stu-id="fad04-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="fad04-124"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fad04-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fad04-125">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fad04-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="fad04-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fad04-126">Remarks</span></span>

<span data-ttu-id="fad04-127">Un entorno de textura especifica cómo se interpretan los valores de textura cuando se textura un fragmento.</span><span class="sxs-lookup"><span data-stu-id="fad04-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="fad04-128">El parámetro de *destino* debe ser de \_ textura GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="fad04-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="fad04-129">El parámetro *PName* puede ser el \_ \_ \_ modo de textura de libro de contabilidad o el color de la textura del libro de contabilidad \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fad04-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="fad04-130">Si *PName* es \_ el modo de textura de libro de contabilidad \_ \_ , entonces *params* es (o señala) el nombre simbólico de una función de textura.</span><span class="sxs-lookup"><span data-stu-id="fad04-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="fad04-131">Se definen tres funciones de textura: libro de contabilidad general \_ , \_ Decal y GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="fad04-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="fad04-132">Una función de textura actúa en el fragmento que se va a texturar mediante el valor de la imagen de textura que se aplica al fragmento (vea [**glTexParameter**](gltexparameter-functions.md)) y genera un color RGBA para ese fragmento.</span><span class="sxs-lookup"><span data-stu-id="fad04-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="fad04-133">En la tabla siguiente se muestra cómo se genera el color RGBA para cada una de las tres funciones de textura que se pueden elegir.</span><span class="sxs-lookup"><span data-stu-id="fad04-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="fad04-134">*C* es un triple de valores de color (RGB) *y es* el valor alfa asociado.</span><span class="sxs-lookup"><span data-stu-id="fad04-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="fad04-135">Los valores RGBA extraídos de una imagen de textura están en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fad04-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="fad04-136">El subíndice *f* hace referencia al fragmento entrante, el subíndice *t* a la imagen de textura, el subíndice *c* al color del entorno de textura y el subíndice *v* indica un valor generado por la función de textura.</span><span class="sxs-lookup"><span data-stu-id="fad04-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="fad04-137">Una imagen de textura puede tener hasta cuatro componentes por elemento de textura (vea [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="fad04-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="fad04-138">En una imagen de un componente, lt indica que se trata de un único componente.</span><span class="sxs-lookup"><span data-stu-id="fad04-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="fad04-139">Una imagen de dos componentes usa *L?*</span><span class="sxs-lookup"><span data-stu-id="fad04-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="fad04-140">y *a?*</span><span class="sxs-lookup"><span data-stu-id="fad04-140">and *A?*</span></span> <span data-ttu-id="fad04-141">.</span><span class="sxs-lookup"><span data-stu-id="fad04-141">.</span></span> <span data-ttu-id="fad04-142">Una imagen de tres componentes solo tiene un valor de color, *C?*</span><span class="sxs-lookup"><span data-stu-id="fad04-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="fad04-143">.</span><span class="sxs-lookup"><span data-stu-id="fad04-143">.</span></span> <span data-ttu-id="fad04-144">Una imagen de cuatro componentes tiene un valor de color *C?*</span><span class="sxs-lookup"><span data-stu-id="fad04-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="fad04-145">y un valor alfa *a?*</span><span class="sxs-lookup"><span data-stu-id="fad04-145">and an alpha value *A?*</span></span> <span data-ttu-id="fad04-146">.</span><span class="sxs-lookup"><span data-stu-id="fad04-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fad04-147">Número de componentes</span><span class="sxs-lookup"><span data-stu-id="fad04-147">Number of components</span></span></th>
<th><span data-ttu-id="fad04-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="fad04-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="fad04-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="fad04-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="fad04-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="fad04-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fad04-151">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fad04-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fad04-152"><em>C<sub>v</sub> </em>   =  <em>¿L?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-152"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="fad04-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fad04-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="fad04-154">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="fad04-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fad04-155"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-155"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="fad04-156"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="fad04-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="fad04-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fad04-158"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fad04-158"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fad04-159"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fad04-159"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fad04-160">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fad04-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fad04-161"><em>C<sub>v</sub> </em>   =  <em>¿L?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-161"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="fad04-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fad04-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="fad04-163">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="fad04-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fad04-164"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-164"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="fad04-165"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="fad04-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="fad04-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fad04-167"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fad04-167"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fad04-168"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fad04-168"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fad04-169">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fad04-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fad04-170"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-170"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="fad04-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fad04-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fad04-172"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-172"><em>C<sub>v</sub></em>  = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="fad04-173">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="fad04-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fad04-174"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="fad04-174"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="fad04-175"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fad04-175"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fad04-176">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fad04-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fad04-177"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-177"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="fad04-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fad04-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fad04-179"><em>C<sub>v</sub> </em> = (1- <em>a?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-179"><em>C<sub>v</sub></em>  = (1 - <em>A?</em></span></span> <span data-ttu-id="fad04-180"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="fad04-181"><em>Unidad?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="fad04-182">$ {REMOVE} $ sin definir</span><span class="sxs-lookup"><span data-stu-id="fad04-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fad04-183"><em>A<sub>v</sub> </em>   =  <em>R?</em></span><span class="sxs-lookup"><span data-stu-id="fad04-183"><em>A<sub>v</sub></em>  = <em>A?</em></span></span> <span data-ttu-id="fad04-184"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="fad04-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="fad04-185"><em>A<sub>v</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fad04-185"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="fad04-186">Si PName es \_ el color de la textura del libro \_ de contabilidad \_ , *params* es un puntero a una matriz que contiene un color RGBA que consta de cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="fad04-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="fad04-187">Los componentes de color entero se interpretan linealmente de forma que el entero más positivo se asigna a 1,0 y el número entero más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="fad04-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="fad04-188">Los valores se fijan en el intervalo \[ 0, 1 \] cuando se especifican.</span><span class="sxs-lookup"><span data-stu-id="fad04-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="fad04-189">*C <sub>c</sub>* toma estos cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="fad04-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="fad04-190">Los \_ \_ valores predeterminados del modo de texturas de contabilidad GL son los valores predeterminados de \_ color modular de GL y textura de GL \_ \_ en (0, 0, \_ \_ 0,0).</span><span class="sxs-lookup"><span data-stu-id="fad04-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="fad04-191">La siguiente función recupera información relacionada con **glTexEnviv**:</span><span class="sxs-lookup"><span data-stu-id="fad04-191">The following function retrieves information related to **glTexEnviv**:</span></span>

[<span data-ttu-id="fad04-192">**glTexGetEnviv**</span><span class="sxs-lookup"><span data-stu-id="fad04-192">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="fad04-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fad04-193">Requirements</span></span>



| <span data-ttu-id="fad04-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad04-194">Requirement</span></span> | <span data-ttu-id="fad04-195">Value</span><span class="sxs-lookup"><span data-stu-id="fad04-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fad04-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fad04-196">Minimum supported client</span></span><br/> | <span data-ttu-id="fad04-197">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fad04-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fad04-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fad04-198">Minimum supported server</span></span><br/> | <span data-ttu-id="fad04-199">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fad04-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fad04-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fad04-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="fad04-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad04-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fad04-202">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fad04-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="fad04-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fad04-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fad04-204">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fad04-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fad04-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad04-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad04-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="fad04-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad04-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fad04-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fad04-208">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fad04-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fad04-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fad04-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fad04-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="fad04-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="fad04-211">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fad04-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





