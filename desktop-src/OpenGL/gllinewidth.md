---
title: función glLineWidth (GL. h)
description: La función glLineWidth especifica el ancho de las líneas rasterizadas.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth (función) OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666083"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="71ee0-104">glLineWidth función)</span><span class="sxs-lookup"><span data-stu-id="71ee0-104">glLineWidth function</span></span>

<span data-ttu-id="71ee0-105">La función **glLineWidth** especifica el ancho de las líneas rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="71ee0-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ee0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71ee0-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="71ee0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71ee0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ee0-108">*width*</span><span class="sxs-lookup"><span data-stu-id="71ee0-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="71ee0-109">Ancho de las líneas rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="71ee0-109">The width of rasterized lines.</span></span> <span data-ttu-id="71ee0-110">El valor predeterminado es 1.0.</span><span class="sxs-lookup"><span data-stu-id="71ee0-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ee0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71ee0-111">Return value</span></span>

<span data-ttu-id="71ee0-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="71ee0-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71ee0-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="71ee0-113">Error codes</span></span>

<span data-ttu-id="71ee0-114">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="71ee0-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71ee0-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="71ee0-115">Name</span></span>                                                                                                  | <span data-ttu-id="71ee0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="71ee0-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71ee0-117"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71ee0-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="71ee0-118">el *ancho* era menor o igual que cero.</span><span class="sxs-lookup"><span data-stu-id="71ee0-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="71ee0-119"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71ee0-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71ee0-120">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="71ee0-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71ee0-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71ee0-121">Remarks</span></span>

<span data-ttu-id="71ee0-122">La función **glLineWidth** especifica el ancho rasterizado de las líneas con alias y antialias.</span><span class="sxs-lookup"><span data-stu-id="71ee0-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="71ee0-123">El uso de un ancho de línea distinto de 1,0 tiene efectos diferentes, en función de si está habilitado el suavizado de línea.</span><span class="sxs-lookup"><span data-stu-id="71ee0-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="71ee0-124">El suavizado de línea se controla mediante una llamada a [**glEnable**](glenable.md) y **glDisable** con el argumento de línea de contabilidad \_ \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="71ee0-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="71ee0-125">Si el suavizado de línea está deshabilitado, el ancho real se determina redondeando el ancho proporcionado al entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="71ee0-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="71ee0-126">(Si el redondeo da como resultado el valor 0,0, es como si el ancho de línea fuera 1,0) \| ¿Si?</span><span class="sxs-lookup"><span data-stu-id="71ee0-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="71ee0-127">x \|  =  \| ?</span><span class="sxs-lookup"><span data-stu-id="71ee0-127">x \| = \| ?</span></span> <span data-ttu-id="71ee0-128">y \| , *i* píxeles se rellenan en cada columna que está rasterizada, donde *i* es el valor redondeado de *ancho*.</span><span class="sxs-lookup"><span data-stu-id="71ee0-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="71ee0-129">De lo contrario, *i* píxeles se rellenan en cada fila que se rasteriza.</span><span class="sxs-lookup"><span data-stu-id="71ee0-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="71ee0-130">Si el suavizado de contorno está habilitado, la rasterización de línea produce un fragmento para cada cuadrado de píxeles que forma una intersección con la región que se encuentra en el rectángulo que tiene un ancho igual al ancho de línea actual, la longitud es igual a la longitud real de la línea y se centra en el segmento de línea matemática.</span><span class="sxs-lookup"><span data-stu-id="71ee0-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="71ee0-131">El valor de cobertura de cada fragmento es el área de coordenadas de la ventana de la intersección de la región rectangular con el cuadrado de píxeles correspondiente.</span><span class="sxs-lookup"><span data-stu-id="71ee0-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="71ee0-132">Este valor se guarda y se usa en el paso de rasterización final.</span><span class="sxs-lookup"><span data-stu-id="71ee0-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="71ee0-133">No se admiten todos los anchos cuando está habilitado el suavizado de línea.</span><span class="sxs-lookup"><span data-stu-id="71ee0-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="71ee0-134">Si se solicita un ancho no compatible, se utiliza el ancho compatible más cercano.</span><span class="sxs-lookup"><span data-stu-id="71ee0-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="71ee0-135">Solo se garantiza la compatibilidad con el ancho 1,0; otros dependen de la implementación.</span><span class="sxs-lookup"><span data-stu-id="71ee0-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="71ee0-136">El intervalo de anchos admitidos y la diferencia de tamaño entre los anchos admitidos en el intervalo se pueden consultar llamando a **glGet** con argumentos \_ rango de ancho de línea de contabilidad \_ \_ y granularidad de ancho de línea de contabilidad \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="71ee0-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="71ee0-137">El ancho de línea especificado por **glLineWidth** siempre se devuelve cuando \_ \_ se consulta el ancho de línea de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="71ee0-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="71ee0-138">La compresión y el redondeo de las líneas con alias y antialias no tienen ningún efecto en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="71ee0-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="71ee0-139">El ancho de línea sin suavizado se puede fijar en un máximo dependiente de la implementación.</span><span class="sxs-lookup"><span data-stu-id="71ee0-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="71ee0-140">Aunque no se puede consultar este máximo, no debe ser menor que el valor máximo de las líneas alisadas, redondeado al valor entero más cercano.</span><span class="sxs-lookup"><span data-stu-id="71ee0-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="71ee0-141">Las siguientes funciones recuperan información relacionada con **glLineWidth**:</span><span class="sxs-lookup"><span data-stu-id="71ee0-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="71ee0-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ ancho de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="71ee0-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="71ee0-143">**glGet** con argumento de \_ ancho de línea de libro de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="71ee0-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="71ee0-144">**glGet** con el argumento \_ \_ granularidad del ancho de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="71ee0-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="71ee0-145">[**glIsEnabled**](glisenabled.md) con el argumento de línea de contabilidad \_ \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="71ee0-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="71ee0-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71ee0-146">Requirements</span></span>



| <span data-ttu-id="71ee0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ee0-147">Requirement</span></span> | <span data-ttu-id="71ee0-148">Value</span><span class="sxs-lookup"><span data-stu-id="71ee0-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ee0-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71ee0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="71ee0-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71ee0-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71ee0-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71ee0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="71ee0-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71ee0-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71ee0-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71ee0-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ee0-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ee0-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71ee0-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71ee0-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="71ee0-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71ee0-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71ee0-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71ee0-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71ee0-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ee0-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ee0-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="71ee0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ee0-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71ee0-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71ee0-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="71ee0-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="71ee0-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71ee0-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71ee0-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="71ee0-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





