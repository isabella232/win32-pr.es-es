---
title: función glBlendFunc (GL. h)
description: La función glBlendFunc especifica la aritmética de píxeles.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc (función) OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686006"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="66d6e-104">glBlendFunc función)</span><span class="sxs-lookup"><span data-stu-id="66d6e-104">glBlendFunc function</span></span>

<span data-ttu-id="66d6e-105">La función **glBlendFunc** especifica la aritmética de píxeles.</span><span class="sxs-lookup"><span data-stu-id="66d6e-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d6e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66d6e-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="66d6e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66d6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d6e-108">*sfactor*</span><span class="sxs-lookup"><span data-stu-id="66d6e-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="66d6e-109">Especifica cómo se calculan los factores de mezcla de origen rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="66d6e-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="66d6e-110">Se aceptan nueve constantes simbólicas: GL \_ Zero, GL \_ One, GL \_ DST \_ color, GL \_ One \_ menos \_ DST \_ color, GL \_ src \_ Alpha, GL \_ One \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha, GL \_ One \_ menos \_ DST \_ Alpha y GL \_ src \_ alpha \_ .</span><span class="sxs-lookup"><span data-stu-id="66d6e-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="66d6e-111">*dfactor*</span><span class="sxs-lookup"><span data-stu-id="66d6e-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="66d6e-112">Especifica cómo se calculan los factores de mezcla de destino rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="66d6e-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="66d6e-113">Se aceptan ocho constantes simbólicas: GL \_ Zero, GL \_ One, GL \_ src \_ color, GL \_ One \_ menos \_ src \_ color, GL \_ src \_ Alpha, GL \_ One \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha y GL \_ One \_ menos \_ DST \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="66d6e-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d6e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66d6e-114">Return value</span></span>

<span data-ttu-id="66d6e-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="66d6e-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66d6e-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="66d6e-116">Error codes</span></span>

<span data-ttu-id="66d6e-117">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="66d6e-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="66d6e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="66d6e-118">Name</span></span>                                                                                                  | <span data-ttu-id="66d6e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="66d6e-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66d6e-120"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d6e-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="66d6e-121">*Sfactor* o *dfactor* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="66d6e-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="66d6e-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d6e-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="66d6e-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="66d6e-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66d6e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d6e-124">Remarks</span></span>

<span data-ttu-id="66d6e-125">En el modo RGB, los píxeles se pueden dibujar con una función que combina los valores RGBA entrantes (origen) con los valores RGBA que ya están en fotogramas (los valores de destino).</span><span class="sxs-lookup"><span data-stu-id="66d6e-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="66d6e-126">De forma predeterminada, la combinación está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="66d6e-126">By default, blending is disabled.</span></span> <span data-ttu-id="66d6e-127">Use [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento de la \_ fusión en contab para habilitar y deshabilitar la fusión.</span><span class="sxs-lookup"><span data-stu-id="66d6e-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="66d6e-128">Cuando está habilitada, **glBlendFunc** define la operación de fusión.</span><span class="sxs-lookup"><span data-stu-id="66d6e-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="66d6e-129">El parámetro *sfactor* especifica los nueve métodos que se usan para escalar los componentes de color de origen.</span><span class="sxs-lookup"><span data-stu-id="66d6e-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="66d6e-130">El parámetro *dfactor* especifica los ocho métodos que se usan para escalar los componentes de color de destino.</span><span class="sxs-lookup"><span data-stu-id="66d6e-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="66d6e-131">Los once métodos posibles se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="66d6e-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="66d6e-132">Cada método define cuatro factores de escala cada uno para rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="66d6e-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="66d6e-133">En la tabla y en las ecuaciones subsiguientes, los componentes de color de origen y destino se conocen como (*R*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="66d6e-134">, *G*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-134">, *G*?</span></span> <span data-ttu-id="66d6e-135">, *B*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-135">, *B*?</span></span> <span data-ttu-id="66d6e-136">, *A*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-136">, *A*?</span></span> <span data-ttu-id="66d6e-137">) y (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="66d6e-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="66d6e-138">Se entiende que tienen valores enteros entre cero y (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>A</sub> ), donde</span><span class="sxs-lookup"><span data-stu-id="66d6e-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="66d6e-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="66d6e-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="66d6e-140">*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1</span><span class="sxs-lookup"><span data-stu-id="66d6e-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="66d6e-141">*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1</span><span class="sxs-lookup"><span data-stu-id="66d6e-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="66d6e-142">*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1</span><span class="sxs-lookup"><span data-stu-id="66d6e-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="66d6e-143">y (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) es el número de bitplaness rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="66d6e-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="66d6e-144">Los factores de escala de origen y destino se conocen como (*s*<sub>r</sub> , *s*<sub>g</sub> , *s*<sub>b</sub> , *s*<sub>a</sub> ) y (*d*<sub>r</sub> , *d*<sub>g</sub> *, d*<sub>b</sub> , *d*<sub>a</sub> ).</span><span class="sxs-lookup"><span data-stu-id="66d6e-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="66d6e-145">Los factores de escala descritos en la tabla, que se indican (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), representan los factores de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="66d6e-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="66d6e-146">Todos los factores de escala tienen el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="66d6e-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="66d6e-147">Parámetro</span><span class="sxs-lookup"><span data-stu-id="66d6e-147">Parameter</span></span>                  | <span data-ttu-id="66d6e-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span><span class="sxs-lookup"><span data-stu-id="66d6e-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d6e-149">GL \_ cero</span><span class="sxs-lookup"><span data-stu-id="66d6e-149">GL\_ZERO</span></span>                   | <span data-ttu-id="66d6e-150">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="66d6e-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="66d6e-151">GL \_ uno</span><span class="sxs-lookup"><span data-stu-id="66d6e-151">GL\_ONE</span></span>                    | <span data-ttu-id="66d6e-152">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="66d6e-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="66d6e-153">\_color de origen del libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="66d6e-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="66d6e-154">(*R*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-154">(*R*?</span></span><span data-ttu-id="66d6e-155"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="66d6e-156"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="66d6e-157"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="66d6e-158"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="66d6e-159">GL \_ uno \_ menos \_ el \_ color src</span><span class="sxs-lookup"><span data-stu-id="66d6e-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="66d6e-160">(1, 1, 1, 1)-(*R*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="66d6e-161"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="66d6e-162"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="66d6e-163"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="66d6e-164"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="66d6e-165">\_color de DST de GL \_</span><span class="sxs-lookup"><span data-stu-id="66d6e-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="66d6e-166">(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="66d6e-167">GL \_ uno \_ menos \_ el \_ color de DST</span><span class="sxs-lookup"><span data-stu-id="66d6e-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="66d6e-168">(1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="66d6e-169">CC \_ src \_ alfa</span><span class="sxs-lookup"><span data-stu-id="66d6e-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="66d6e-170">(*A*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-170">(*A*?</span></span><span data-ttu-id="66d6e-171"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="66d6e-172"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="66d6e-173"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="66d6e-174"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="66d6e-175">GL \_ uno \_ menos \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="66d6e-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="66d6e-176">(1, 1, 1, 1)-(*a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="66d6e-177"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="66d6e-178"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="66d6e-179"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="66d6e-180"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="66d6e-181">GL \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="66d6e-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="66d6e-182">(*A*<sub>d</sub>  /  *k*<sub>a</sub> , *d*<sub></sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="66d6e-183">GL \_ uno \_ menos \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="66d6e-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="66d6e-184">(1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , d <sub></sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="66d6e-185">libro de contabilidad \_ orig \_ alfa \_ saturado</span><span class="sxs-lookup"><span data-stu-id="66d6e-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="66d6e-186">(*i* , i, 1)</span><span class="sxs-lookup"><span data-stu-id="66d6e-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="66d6e-187">En la tabla,</span><span class="sxs-lookup"><span data-stu-id="66d6e-187">In the table,</span></span>

<span data-ttu-id="66d6e-188">*i* = min (*A*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-188">*i* = min (*A*?</span></span> <span data-ttu-id="66d6e-189">, *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="66d6e-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="66d6e-190">Para determinar los valores RGBA combinados de un píxel al dibujar en el modo RGBA, el sistema usa las ecuaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="66d6e-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="66d6e-191">*R* (*d*) = mín ( *k*<sub>r</sub> , *r*? *s*<sub>r</sub>  +  <sub>d</sub> *d*<sub>r</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="66d6e-192">*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  <sub>d</sub> <sub>g</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="66d6e-193">*B* (*d*) = min ( *k*<sub>B</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *d*<sub>b</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="66d6e-194">*A* (*d*) = min ( *k*<sub>a</sub> , *a*? *s*<sub>a</sub>  +  <sub>d</sub> *d*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="66d6e-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="66d6e-195">A pesar de la precisión aparente de las ecuaciones anteriores, la aritmética de mezcla no se especifica exactamente, ya que la mezcla funciona con valores de color enteros imprecisos.</span><span class="sxs-lookup"><span data-stu-id="66d6e-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="66d6e-196">Sin embargo, se garantiza que un factor de mezcla que debe ser igual a uno no modifique su multiplicando y un factor de mezcla igual a cero reduce su multiplicando a cero.</span><span class="sxs-lookup"><span data-stu-id="66d6e-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="66d6e-197">Por lo tanto, por ejemplo, cuando *sfactor* es GL \_ src \_ Alpha, *dfactor* es GL \_ One \_ menos \_ src \_ Alpha y *a*? es igual a *k* a, las ecuaciones se reducen a <sub>un</sub>reemplazo sencillo:</span><span class="sxs-lookup"><span data-stu-id="66d6e-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="66d6e-198">*R*<sub>d</sub>  =  *r*</span><span class="sxs-lookup"><span data-stu-id="66d6e-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="66d6e-199">*G*<sub>d</sub>  =  *g*</span><span class="sxs-lookup"><span data-stu-id="66d6e-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="66d6e-200">B <sub>d</sub>  =  *b*?</span><span class="sxs-lookup"><span data-stu-id="66d6e-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="66d6e-201">*Una*<sub>d</sub>  =  ?</span><span class="sxs-lookup"><span data-stu-id="66d6e-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="66d6e-202">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="66d6e-202">Examples</span></span>

<span data-ttu-id="66d6e-203">La transparencia se implementa mejor mediante **glBlendFunc**(GL \_ src \_ Alpha, GL \_ One \_ menos \_ src \_ Alpha) con primitivas ordenadas de más lejos a más próxima.</span><span class="sxs-lookup"><span data-stu-id="66d6e-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="66d6e-204">Tenga en cuenta que este cálculo de transparencia no requiere la presencia de alfa bitplanes en fotogramas.</span><span class="sxs-lookup"><span data-stu-id="66d6e-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="66d6e-205">También puede usar **glBlendFunc**(GL \_ src \_ Alpha, GL \_ uno \_ menos \_ src \_ Alpha) para representar puntos y líneas con suavizado de contorno en orden arbitrario.</span><span class="sxs-lookup"><span data-stu-id="66d6e-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="66d6e-206">Para optimizar el suavizado de contorno de polígono, use **glBlendFunc**(GL \_ src \_ alfa \_ Saturate, GL \_ uno) con polígonos ordenados de más cercano a más alejados.</span><span class="sxs-lookup"><span data-stu-id="66d6e-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="66d6e-207">(Vea el libro de contabilidad \_ \_Argumento de Polígono suave en [**glEnable**](glenable.md) para obtener información sobre el suavizado de contorno de polígono). Destino Alfa bitplanes, que debe estar presente para que esta función de Blend funcione correctamente, almacene la cobertura acumulada.</span><span class="sxs-lookup"><span data-stu-id="66d6e-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="66d6e-208">El alfa entrante (origen) es una opacidad material, que va desde 1,0 (*K*<sub>a</sub> ), que representa la opacidad completa hasta 0,0 (0), que representa una transparencia completa.</span><span class="sxs-lookup"><span data-stu-id="66d6e-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="66d6e-209">Cuando se habilita más de un búfer de color para dibujar, cada búfer habilitado se mezcla por separado y el contenido del búfer se usa para el color de destino.</span><span class="sxs-lookup"><span data-stu-id="66d6e-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="66d6e-210">(Consulte [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="66d6e-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="66d6e-211">La mezcla solo afecta a la representación RGBA.</span><span class="sxs-lookup"><span data-stu-id="66d6e-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="66d6e-212">Lo omiten los representadores de índice de color.</span><span class="sxs-lookup"><span data-stu-id="66d6e-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="66d6e-213">Las siguientes funciones recuperan información relacionada con **glBlendFunc**:</span><span class="sxs-lookup"><span data-stu-id="66d6e-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="66d6e-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento CC \_ Blend \_ src</span><span class="sxs-lookup"><span data-stu-id="66d6e-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="66d6e-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ Blend \_ DST</span><span class="sxs-lookup"><span data-stu-id="66d6e-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="66d6e-216">[**glIsEnabled**](glisenabled.md) con argumento de GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="66d6e-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="66d6e-217">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d6e-217">Requirements</span></span>



| <span data-ttu-id="66d6e-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d6e-218">Requirement</span></span> | <span data-ttu-id="66d6e-219">Value</span><span class="sxs-lookup"><span data-stu-id="66d6e-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66d6e-220">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d6e-220">Minimum supported client</span></span><br/> | <span data-ttu-id="66d6e-221">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="66d6e-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66d6e-222">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d6e-222">Minimum supported server</span></span><br/> | <span data-ttu-id="66d6e-223">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66d6e-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66d6e-224">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66d6e-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d6e-225"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d6e-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="66d6e-226">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66d6e-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="66d6e-227"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66d6e-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="66d6e-228">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66d6e-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66d6e-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66d6e-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d6e-230">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d6e-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d6e-231">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="66d6e-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="66d6e-232">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="66d6e-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="66d6e-233">**glClear**</span><span class="sxs-lookup"><span data-stu-id="66d6e-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="66d6e-234">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="66d6e-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="66d6e-235">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="66d6e-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="66d6e-236">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="66d6e-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="66d6e-237">**glGet**</span><span class="sxs-lookup"><span data-stu-id="66d6e-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="66d6e-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="66d6e-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="66d6e-239">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="66d6e-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="66d6e-240">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="66d6e-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





