---
title: función glLineStipple (GL. h)
description: La función glLineStipple especifica el patrón punteado de línea.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple (función) OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800998"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="56ad0-104">glLineStipple función)</span><span class="sxs-lookup"><span data-stu-id="56ad0-104">glLineStipple function</span></span>

<span data-ttu-id="56ad0-105">La función **glLineStipple** especifica el patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="56ad0-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ad0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56ad0-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="56ad0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56ad0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ad0-108">*diez*</span><span class="sxs-lookup"><span data-stu-id="56ad0-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="56ad0-109">Un multiplicador para cada bit en el patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="56ad0-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="56ad0-110">Si *factor* es 3, por ejemplo, cada bit del patrón se usará tres veces antes de que se use el siguiente bit del patrón.</span><span class="sxs-lookup"><span data-stu-id="56ad0-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="56ad0-111">El parámetro *factor* se fija en el intervalo \[ 1, 256 y el \] valor predeterminado es uno.</span><span class="sxs-lookup"><span data-stu-id="56ad0-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="56ad0-112">*pattern*</span><span class="sxs-lookup"><span data-stu-id="56ad0-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="56ad0-113">Entero de 16 bits cuyo modelo de bits determina qué fragmentos de una línea se dibujarán cuando se rasteriza la línea.</span><span class="sxs-lookup"><span data-stu-id="56ad0-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="56ad0-114">Primero se usa el bit cero y el patrón predeterminado es todos.</span><span class="sxs-lookup"><span data-stu-id="56ad0-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ad0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56ad0-115">Return value</span></span>

<span data-ttu-id="56ad0-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="56ad0-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56ad0-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="56ad0-117">Error codes</span></span>

<span data-ttu-id="56ad0-118">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="56ad0-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="56ad0-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="56ad0-119">Name</span></span>                                                                                                  | <span data-ttu-id="56ad0-120">Significado</span><span class="sxs-lookup"><span data-stu-id="56ad0-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56ad0-121"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56ad0-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="56ad0-122">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="56ad0-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="56ad0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56ad0-123">Remarks</span></span>

<span data-ttu-id="56ad0-124">La función **glLineStipple** especifica el patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="56ad0-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="56ad0-125">El punteado de línea oculta determinados fragmentos producidos por la rasterización; esos fragmentos no se dibujarán.</span><span class="sxs-lookup"><span data-stu-id="56ad0-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="56ad0-126">El enmascaramiento se consigue con tres parámetros: el *patrón* de patrón punteado de línea de 16 bits, el *factor* de recuento de repetición y un contador de entero punteado *s*.</span><span class="sxs-lookup"><span data-stu-id="56ad0-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="56ad0-127">Counter *s* se restablece a cero cada vez que se llama a [**glBegin**](glbegin.md) y antes de que se genere cada segmento de línea de una secuencia de **glBegin**(líneas de contabilidad \_ )/**glEnd** .</span><span class="sxs-lookup"><span data-stu-id="56ad0-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="56ad0-128">Se incrementa después de que se genere cada fragmento de un segmento de línea con alias de ancho de unidad, o después de que se generen todos los fragmentos *i* de un segmento de línea *i* width.</span><span class="sxs-lookup"><span data-stu-id="56ad0-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="56ad0-129">Los fragmentos *i* asociados a los *recuentos* se enmascaran si el bit de *patrón* (*s*  /  *factor*) mod 16 es cero.</span><span class="sxs-lookup"><span data-stu-id="56ad0-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="56ad0-130">De lo contrario, estos fragmentos se envían a fotogramas.</span><span class="sxs-lookup"><span data-stu-id="56ad0-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="56ad0-131">El bit cero del *patrón* es el bit menos significativo.</span><span class="sxs-lookup"><span data-stu-id="56ad0-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="56ad0-132">Las líneas con suavizado de contorno se tratan como una secuencia de 1x rectángulos de *ancho* para los fines de este.</span><span class="sxs-lookup"><span data-stu-id="56ad0-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="56ad0-133">Rectangle *s* se rasteriza o no se basa en la regla de fragmento descrita para las líneas con alias; cuenta los rectángulos en lugar de los grupos de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="56ad0-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="56ad0-134">El punteado de líneas está habilitado o deshabilitado mediante [**glEnable**](glenable.md) y **glDisable** con el argumento de línea de contabilidad \_ \_ punteada.</span><span class="sxs-lookup"><span data-stu-id="56ad0-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="56ad0-135">Cuando está habilitado, el patrón punteado de línea se aplica como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="56ad0-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="56ad0-136">Cuando está deshabilitado, es como si el patrón fuera todo.</span><span class="sxs-lookup"><span data-stu-id="56ad0-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="56ad0-137">Inicialmente, la línea punteada está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="56ad0-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="56ad0-138">Las siguientes funciones recuperan información relacionada con **glLineStipple**:</span><span class="sxs-lookup"><span data-stu-id="56ad0-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="56ad0-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ \_ patrón punteado de línea de contabilidad de argumento \_</span><span class="sxs-lookup"><span data-stu-id="56ad0-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="56ad0-140">**glGet** con argumento de \_ línea de contabilidad \_ punteada \_</span><span class="sxs-lookup"><span data-stu-id="56ad0-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="56ad0-141">[**glIsEnabled**](glisenabled.md) con el argumento \_ línea de contabilidad \_ punteada</span><span class="sxs-lookup"><span data-stu-id="56ad0-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="56ad0-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ad0-142">Requirements</span></span>



| <span data-ttu-id="56ad0-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ad0-143">Requirement</span></span> | <span data-ttu-id="56ad0-144">Value</span><span class="sxs-lookup"><span data-stu-id="56ad0-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56ad0-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56ad0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="56ad0-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="56ad0-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56ad0-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56ad0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="56ad0-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56ad0-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56ad0-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56ad0-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ad0-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ad0-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="56ad0-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56ad0-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="56ad0-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56ad0-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="56ad0-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56ad0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ad0-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ad0-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ad0-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="56ad0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ad0-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="56ad0-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="56ad0-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="56ad0-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="56ad0-158">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="56ad0-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="56ad0-159">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="56ad0-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





