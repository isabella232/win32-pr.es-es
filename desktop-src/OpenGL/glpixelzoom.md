---
title: función glPixelZoom (GL. h)
description: La función glPixelZoom especifica los factores de zoom de píxeles.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glPixelZoom (función) OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105670051"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="b0b03-104">glPixelZoom función)</span><span class="sxs-lookup"><span data-stu-id="b0b03-104">glPixelZoom function</span></span>

<span data-ttu-id="b0b03-105">La función **glPixelZoom** especifica los factores de zoom de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b0b03-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b03-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0b03-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="b0b03-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0b03-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b03-108">*xfactor*</span><span class="sxs-lookup"><span data-stu-id="b0b03-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b03-109">Factor de zoom *x* para las operaciones de escritura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b0b03-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="b0b03-110">*yfactor*</span><span class="sxs-lookup"><span data-stu-id="b0b03-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b03-111">Factor de zoom *y* para las operaciones de escritura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b0b03-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b03-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0b03-112">Return value</span></span>

<span data-ttu-id="b0b03-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b0b03-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0b03-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b0b03-114">Error codes</span></span>

<span data-ttu-id="b0b03-115">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="b0b03-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b0b03-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b0b03-116">Name</span></span>                                                                                                  | <span data-ttu-id="b0b03-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b0b03-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0b03-118"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b03-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0b03-119">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b0b03-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b0b03-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0b03-120">Remarks</span></span>

<span data-ttu-id="b0b03-121">La función **glPixelZoom** especifica valores para los factores de zoom *x* *e y.*</span><span class="sxs-lookup"><span data-stu-id="b0b03-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="b0b03-122">Durante la ejecución de [**glDrawPixels**](gldrawpixels.md) o [**glCopyPixels**](glcopypixels.md), si (*x*<sub>r</sub> ,*y*<sub>r</sub> ) es la posición de la trama actual y un elemento determinado está en la fila *n* y la columna *m* del rectángulo de píxeles, los píxeles cuyos centros se encuentran en el rectángulo con esquinas en</span><span class="sxs-lookup"><span data-stu-id="b0b03-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![Ecuación que muestra las ubicaciones en las que los píxeles son candidatos para el reemplazo.](images/pix05.png)

<span data-ttu-id="b0b03-124">son candidatas para el reemplazo.</span><span class="sxs-lookup"><span data-stu-id="b0b03-124">are candidates for replacement.</span></span> <span data-ttu-id="b0b03-125">También se modifica cualquier píxel cuyo centro se encuentre en el borde inferior o izquierdo de esta región rectangular.</span><span class="sxs-lookup"><span data-stu-id="b0b03-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="b0b03-126">Los factores de zoom en píxeles no se limitan a los valores positivos.</span><span class="sxs-lookup"><span data-stu-id="b0b03-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="b0b03-127">Los factores de zoom negativos reflejan la imagen resultante sobre la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="b0b03-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="b0b03-128">Las siguientes funciones recuperan información relacionada con **glPixelZoom**:</span><span class="sxs-lookup"><span data-stu-id="b0b03-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="b0b03-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ zoom \_ X</span><span class="sxs-lookup"><span data-stu-id="b0b03-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="b0b03-130">**glGet** con el argumento \_ zoom de GL \_ Y</span><span class="sxs-lookup"><span data-stu-id="b0b03-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b03-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b03-131">Requirements</span></span>



| <span data-ttu-id="b0b03-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b03-132">Requirement</span></span> | <span data-ttu-id="b0b03-133">Value</span><span class="sxs-lookup"><span data-stu-id="b0b03-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b03-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b03-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b03-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b0b03-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0b03-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b03-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b03-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0b03-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0b03-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0b03-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b03-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b03-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b0b03-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0b03-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0b03-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0b03-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0b03-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0b03-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0b03-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0b03-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b03-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0b03-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b03-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b0b03-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b0b03-146">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="b0b03-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="b0b03-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="b0b03-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b0b03-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0b03-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





