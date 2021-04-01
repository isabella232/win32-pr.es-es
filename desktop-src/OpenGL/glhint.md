---
title: función glHint (GL. h)
description: La función glHint especifica sugerencias específicas de la implementación.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint (función) OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150052"
---
# <a name="glhint-function"></a><span data-ttu-id="ddfc9-104">glHint función)</span><span class="sxs-lookup"><span data-stu-id="ddfc9-104">glHint function</span></span>

<span data-ttu-id="ddfc9-105">La función **glHint** especifica sugerencias específicas de la implementación.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddfc9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddfc9-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ddfc9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddfc9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddfc9-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="ddfc9-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="ddfc9-109">Constante simbólica que indica el comportamiento que se va a controlar.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="ddfc9-110">Se aceptan las siguientes constantes simbólicas, junto con la semántica sugerida.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="ddfc9-111">Value</span><span class="sxs-lookup"><span data-stu-id="ddfc9-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="ddfc9-112">Significado</span><span class="sxs-lookup"><span data-stu-id="ddfc9-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="ddfc9-113"><dt>**\_sugerencia de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="ddfc9-114">Indica la precisión del cálculo de niebla.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="ddfc9-115">Si el cálculo de la niebla por píxel no se admite de forma eficaz en la implementación de OpenGL, la sugerencia de libro de contabilidad no se tiene \_ \_ en cuenta o la \_ más rápida puede dar lugar a un cálculo por vértices de los efectos de niebla.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="ddfc9-116"><dt>**\_sugerencia de \_ suavizado de línea de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="ddfc9-117">Indica la calidad de muestreo de las líneas con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="ddfc9-118">\_La sugerencia de libro de contabilidad puede dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función de filtro más grande.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="ddfc9-119"><dt>**\_sugerencia de \_ corrección de perspectiva de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="ddfc9-120">Indica la calidad de la interpolación de coordenadas de color y textura.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="ddfc9-121">Si la implementación de OpenGL no admite la interpolación de parámetros corregidos por perspectiva de forma eficaz, la sugerencia del libro de contabilidad no se tiene \_ \_ en cuenta o la \_ más rápida puede producir una interpolación lineal simple de colores y/o coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="ddfc9-122"><dt>**\_ \_ sugerencia Smooth de punto de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="ddfc9-123">Indica la calidad de muestreo de los puntos antialias.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="ddfc9-124">\_La sugerencia de libro de contabilidad puede dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función de filtro más grande.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="ddfc9-125"><dt>**\_ \_ sugerencia Smooth de polígono de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="ddfc9-126">Indica la calidad de muestreo de los polígonos con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="ddfc9-127">\_La sugerencia de libro de contabilidad puede dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función de filtro más grande.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="ddfc9-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="ddfc9-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ddfc9-129">Constante simbólica que indica el comportamiento deseado.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="ddfc9-130">Se aceptan las siguientes constantes simbólicas.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="ddfc9-131">Value</span><span class="sxs-lookup"><span data-stu-id="ddfc9-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="ddfc9-132">Significado</span><span class="sxs-lookup"><span data-stu-id="ddfc9-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="ddfc9-133"><dt>**GL \_ más rápido**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="ddfc9-134">Se debe elegir la opción más eficaz.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="ddfc9-135"><dt>**libro \_ de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="ddfc9-136">Se debe elegir la opción más adecuada o de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="ddfc9-137"><dt>**no importa el libro de contabilidad \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="ddfc9-138">El cliente no tiene ninguna preferencia.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddfc9-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddfc9-139">Return value</span></span>

<span data-ttu-id="ddfc9-140">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ddfc9-141">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ddfc9-141">Error codes</span></span>

<span data-ttu-id="ddfc9-142">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ddfc9-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddfc9-143">Name</span></span>                                                                                                  | <span data-ttu-id="ddfc9-144">Significado</span><span class="sxs-lookup"><span data-stu-id="ddfc9-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ddfc9-145"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ddfc9-146">el *destino* o el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="ddfc9-147"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ddfc9-148">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ddfc9-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ddfc9-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddfc9-149">Remarks</span></span>

<span data-ttu-id="ddfc9-150">Cuando hay espacio para la interpretación, puede controlar ciertos aspectos del comportamiento de OpenGL con sugerencias.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="ddfc9-151">Especifique una sugerencia con dos argumentos.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="ddfc9-152">El parámetro de *destino* es una constante simbólica que indica el comportamiento que se va a controlar y el *modo* es otra constante simbólica que indica el comportamiento deseado.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="ddfc9-153">Aunque los aspectos de implementación que se pueden sugerir están bien definidos, la interpretación de las sugerencias depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="ddfc9-154">La función **glHint** se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddfc9-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddfc9-155">Requirements</span></span>



| <span data-ttu-id="ddfc9-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddfc9-156">Requirement</span></span> | <span data-ttu-id="ddfc9-157">Value</span><span class="sxs-lookup"><span data-stu-id="ddfc9-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddfc9-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddfc9-158">Minimum supported client</span></span><br/> | <span data-ttu-id="ddfc9-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ddfc9-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ddfc9-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddfc9-160">Minimum supported server</span></span><br/> | <span data-ttu-id="ddfc9-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddfc9-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ddfc9-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddfc9-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddfc9-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ddfc9-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddfc9-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddfc9-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ddfc9-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddfc9-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddfc9-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddfc9-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddfc9-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddfc9-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ddfc9-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ddfc9-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ddfc9-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





