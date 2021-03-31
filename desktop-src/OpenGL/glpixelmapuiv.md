---
title: función glPixelMapuiv (GL. h)
description: La función glPixelMapuiv configura mapas de transferencia de píxeles.
ms.assetid: dd0f7881-fdd1-49c2-b68c-21e2f9e5ecd2
keywords:
- glPixelMapuiv (función) OpenGL
topic_type:
- apiref
api_name:
- glPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9b31398060e62fa14cd35afe4f8536dd78f963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996522"
---
# <a name="glpixelmapuiv-function"></a><span data-ttu-id="68b5a-104">glPixelMapuiv función)</span><span class="sxs-lookup"><span data-stu-id="68b5a-104">glPixelMapuiv function</span></span>

<span data-ttu-id="68b5a-105">La función **glPixelMapuiv** configura mapas de transferencia de píxeles.</span><span class="sxs-lookup"><span data-stu-id="68b5a-105">The **glPixelMapuiv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b5a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68b5a-106">Syntax</span></span>


```C++
void WINAPI glPixelMapuiv(
         GLenum  map,
         GLsizei mapsize,
   const GLuint  *values
);
```



## <a name="parameters"></a><span data-ttu-id="68b5a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68b5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b5a-108">*map*</span><span class="sxs-lookup"><span data-stu-id="68b5a-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="68b5a-109">Un nombre de asignación simbólico.</span><span class="sxs-lookup"><span data-stu-id="68b5a-109">A symbolic map name.</span></span> <span data-ttu-id="68b5a-110">Las diez asignaciones son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="68b5a-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="68b5a-111">Value</span><span class="sxs-lookup"><span data-stu-id="68b5a-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="68b5a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="68b5a-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="68b5a-113"><dt>**\_ \_ mapa de píxeles \_ \_ de \_ Contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="68b5a-114">Asigna índices de color a los índices de color.</span><span class="sxs-lookup"><span data-stu-id="68b5a-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="68b5a-115"><dt>**\_ \_ asignación de píxeles \_ de GL s \_ a \_ s**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="68b5a-116">Asigna los índices de estarcido a los índices de estarcido.</span><span class="sxs-lookup"><span data-stu-id="68b5a-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="68b5a-117"><dt>**\_ \_ mapa de píxeles \_ de GL I \_ a \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="68b5a-118">Asigna índices de color a componentes rojos.</span><span class="sxs-lookup"><span data-stu-id="68b5a-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="68b5a-119"><dt>**\_ \_ mapa de píxeles \_ de GL I \_ a \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="68b5a-120">Asigna índices de color a componentes verdes.</span><span class="sxs-lookup"><span data-stu-id="68b5a-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="68b5a-121"><dt>**\_ \_ mapa de píxeles \_ de GL I \_ a \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="68b5a-122">Asigna índices de color a los componentes azules.</span><span class="sxs-lookup"><span data-stu-id="68b5a-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="68b5a-123"><dt>**\_mapa de \_ píxeles \_ \_ de \_ Contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="68b5a-124">Asigna índices de color a componentes alfa.</span><span class="sxs-lookup"><span data-stu-id="68b5a-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="68b5a-125"><dt>**\_ \_ mapa de píxeles \_ de GL R \_ a \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="68b5a-126">Asigna componentes rojos a componentes rojos.</span><span class="sxs-lookup"><span data-stu-id="68b5a-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="68b5a-127"><dt>**\_ \_ mapa de píxeles \_ de GL G \_ a \_ g**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="68b5a-128">Asigna los componentes verdes a los componentes verdes.</span><span class="sxs-lookup"><span data-stu-id="68b5a-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="68b5a-129"><dt>**\_ \_ mapa de píxeles \_ de contabilidad B \_ a \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="68b5a-130">Asigna componentes azules a componentes azules.</span><span class="sxs-lookup"><span data-stu-id="68b5a-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="68b5a-131"><dt>**\_ \_ \_ la asignación de píxeles de GL \_ a a \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="68b5a-132">Asigna los componentes alfa a los componentes alfa.</span><span class="sxs-lookup"><span data-stu-id="68b5a-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="68b5a-133">*asignar*</span><span class="sxs-lookup"><span data-stu-id="68b5a-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="68b5a-134">Tamaño del mapa que se está definiendo.</span><span class="sxs-lookup"><span data-stu-id="68b5a-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="68b5a-135">*Valores*</span><span class="sxs-lookup"><span data-stu-id="68b5a-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="68b5a-136">Matriz de valores de *asignación* .</span><span class="sxs-lookup"><span data-stu-id="68b5a-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b5a-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68b5a-137">Return value</span></span>

<span data-ttu-id="68b5a-138">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="68b5a-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68b5a-139">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="68b5a-139">Error codes</span></span>

<span data-ttu-id="68b5a-140">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="68b5a-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="68b5a-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="68b5a-141">Name</span></span>                                                                                                  | <span data-ttu-id="68b5a-142">Significado</span><span class="sxs-lookup"><span data-stu-id="68b5a-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68b5a-143"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="68b5a-144">la *asignación* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="68b5a-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="68b5a-145"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="68b5a-146">el valor de la asignación *es negativo* o mayor que el de la tabla de mapa de píxeles de contabilidad \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68b5a-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="68b5a-147"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="68b5a-148">*map era el* mapa de píxeles de contabilidad \_ \_ \_ i \_ a \_ i, el \_ mapa de píxeles de GL \_ \_ s \_ a \_ s, el mapa de píxeles de GL \_ \_ \_ i \_ a \_ R, \_ el mapa de píxeles de GL \_ \_ i \_ a \_ G, el mapa de \_ píxeles de GL \_ \_ i \_ a \_ B o \_ el mapa de píxeles de GL \_ \_ i a a \_ , y la asignación \_ no era una potencia de dos. </span><span class="sxs-lookup"><span data-stu-id="68b5a-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="68b5a-149"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="68b5a-150">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="68b5a-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="68b5a-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68b5a-151">Remarks</span></span>

<span data-ttu-id="68b5a-152">La función **glPixelMap** configura las tablas de traducción, o *asignaciones*, utilizadas [**por glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="68b5a-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="68b5a-153">El uso de estas asignaciones se describe completamente en el tema [**glPixelTransfer**](glpixeltransfer.md) y, en parte, en los temas para los comandos píxel y imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="68b5a-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="68b5a-154">En este tema solo se describe la especificación de las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="68b5a-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="68b5a-155">El parámetro de *asignación* es un nombre de mapa simbólico, que indica una de las diez asignaciones que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="68b5a-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="68b5a-156">El *parámetro de asignación especifica* el número de entradas en el mapa y *los valores* son un puntero a una matriz de valores de mapa de *asignaciones* .</span><span class="sxs-lookup"><span data-stu-id="68b5a-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="68b5a-157">Las entradas de un mapa se pueden especificar como números de punto flotante de precisión sencilla, enteros cortos sin signo o enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="68b5a-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="68b5a-158">Asignaciones que almacenan los valores de los componentes de color (todos los elementos, pero el mapa de píxeles de contabilidad \_ \_ \_ i y los mapas de píxeles de libro de contabilidad \_ \_ \_ \_ \_ \_ a \_ s) conservan sus valores en formato de punto flotante, con un tamaño no especificado de la mantisa y el exponente.</span><span class="sxs-lookup"><span data-stu-id="68b5a-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="68b5a-159">Los valores de punto flotante especificados por [**glPixelMapfv**](glpixelmap.md) se convierten directamente al formato de punto flotante interno de estas asignaciones y, a continuación, se fijan en el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="68b5a-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="68b5a-160">Los valores enteros sin signo especificados por **glPixelMapusv** y **glPixelMapuiv** se convierten linealmente de forma que el entero más grande que se puede representar se asigna a 1,0 y cero se asigna a 0,0.</span><span class="sxs-lookup"><span data-stu-id="68b5a-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="68b5a-161">Asignaciones que almacenan índices, \_ \_ el mapa de píxeles de contabilidad \_ i \_ \_ y \_ los mapas de píxeles de contabilidad de \_ \_ \_ la serie s a \_ s, conservan sus valores en formato de punto fijo, con un número no especificado de bits a la derecha del punto binario.</span><span class="sxs-lookup"><span data-stu-id="68b5a-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="68b5a-162">Los valores de punto flotante especificados por [**glPixelMapfv**](glpixelmap.md) se convierten directamente en el formato de punto fijo interno de estas asignaciones.</span><span class="sxs-lookup"><span data-stu-id="68b5a-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="68b5a-163">Los valores enteros sin signo especificados por **glPixelMapusv** y **glPixelMapuiv** especifican valores enteros, con todos los ceros a la derecha del punto binario.</span><span class="sxs-lookup"><span data-stu-id="68b5a-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="68b5a-164">En la tabla siguiente se muestran los tamaños iniciales y los valores de cada uno de los mapas.</span><span class="sxs-lookup"><span data-stu-id="68b5a-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="68b5a-165">Los mapas que se indexan mediante índices de color o de estarcido deben tener el *asignador* = 2 ^ *n* para algunos *n* o los resultados no están definidos.</span><span class="sxs-lookup"><span data-stu-id="68b5a-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="68b5a-166">El tamaño máximo permitido para cada mapa depende de la implementación y se puede determinar mediante una llamada a **glGet** con la \_ tabla de mapa de píxeles Max Max argument \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68b5a-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="68b5a-167">El máximo único se aplica a todos los mapas y es al menos 32.</span><span class="sxs-lookup"><span data-stu-id="68b5a-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="68b5a-168">Map</span><span class="sxs-lookup"><span data-stu-id="68b5a-168">Map</span></span>                      | <span data-ttu-id="68b5a-169">Índice de búsqueda</span><span class="sxs-lookup"><span data-stu-id="68b5a-169">Lookup Index</span></span>  | <span data-ttu-id="68b5a-170">Valor de búsqueda</span><span class="sxs-lookup"><span data-stu-id="68b5a-170">Lookup Value</span></span>  | <span data-ttu-id="68b5a-171">Tamaño inicial</span><span class="sxs-lookup"><span data-stu-id="68b5a-171">Initial Size</span></span> | <span data-ttu-id="68b5a-172">Valor inicial</span><span class="sxs-lookup"><span data-stu-id="68b5a-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="68b5a-173">\_ \_ mapa de píxeles \_ \_ de \_ Contabilidad</span><span class="sxs-lookup"><span data-stu-id="68b5a-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="68b5a-174">Índice de color</span><span class="sxs-lookup"><span data-stu-id="68b5a-174">color index</span></span>   | <span data-ttu-id="68b5a-175">Índice de color</span><span class="sxs-lookup"><span data-stu-id="68b5a-175">color index</span></span>   | <span data-ttu-id="68b5a-176">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-176">1</span></span>            | <span data-ttu-id="68b5a-177">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-177">0.0</span></span>           |
| <span data-ttu-id="68b5a-178">\_ \_ asignación de píxeles \_ de GL s \_ a \_ s</span><span class="sxs-lookup"><span data-stu-id="68b5a-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="68b5a-179">Índice de estarcido</span><span class="sxs-lookup"><span data-stu-id="68b5a-179">stencil index</span></span> | <span data-ttu-id="68b5a-180">Índice de estarcido</span><span class="sxs-lookup"><span data-stu-id="68b5a-180">stencil index</span></span> | <span data-ttu-id="68b5a-181">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-181">1</span></span>            | <span data-ttu-id="68b5a-182">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-182">0.0</span></span>           |
| <span data-ttu-id="68b5a-183">\_ \_ mapa de píxeles \_ de GL I \_ a \_ R</span><span class="sxs-lookup"><span data-stu-id="68b5a-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="68b5a-184">Índice de color</span><span class="sxs-lookup"><span data-stu-id="68b5a-184">color index</span></span>   | <span data-ttu-id="68b5a-185">R</span><span class="sxs-lookup"><span data-stu-id="68b5a-185">R</span></span>             | <span data-ttu-id="68b5a-186">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-186">1</span></span>            | <span data-ttu-id="68b5a-187">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-187">0.0</span></span>           |
| <span data-ttu-id="68b5a-188">\_ \_ mapa de píxeles \_ de GL I \_ a \_ G</span><span class="sxs-lookup"><span data-stu-id="68b5a-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="68b5a-189">Índice de color</span><span class="sxs-lookup"><span data-stu-id="68b5a-189">color index</span></span>   | <span data-ttu-id="68b5a-190">G</span><span class="sxs-lookup"><span data-stu-id="68b5a-190">G</span></span>             | <span data-ttu-id="68b5a-191">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-191">1</span></span>            | <span data-ttu-id="68b5a-192">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-192">0.0</span></span>           |
| <span data-ttu-id="68b5a-193">\_ \_ mapa de píxeles \_ de GL I \_ a \_ B</span><span class="sxs-lookup"><span data-stu-id="68b5a-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="68b5a-194">Índice de color</span><span class="sxs-lookup"><span data-stu-id="68b5a-194">color index</span></span>   | <span data-ttu-id="68b5a-195">B</span><span class="sxs-lookup"><span data-stu-id="68b5a-195">B</span></span>             | <span data-ttu-id="68b5a-196">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-196">1</span></span>            | <span data-ttu-id="68b5a-197">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-197">0.0</span></span>           |
| <span data-ttu-id="68b5a-198">\_mapa de \_ píxeles \_ \_ de \_ Contabilidad</span><span class="sxs-lookup"><span data-stu-id="68b5a-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="68b5a-199">Índice de color</span><span class="sxs-lookup"><span data-stu-id="68b5a-199">color index</span></span>   | <span data-ttu-id="68b5a-200">A</span><span class="sxs-lookup"><span data-stu-id="68b5a-200">A</span></span>             | <span data-ttu-id="68b5a-201">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-201">1</span></span>            | <span data-ttu-id="68b5a-202">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-202">0.0</span></span>           |
| <span data-ttu-id="68b5a-203">\_ \_ mapa de píxeles \_ de GL R \_ a \_ r</span><span class="sxs-lookup"><span data-stu-id="68b5a-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="68b5a-204">R</span><span class="sxs-lookup"><span data-stu-id="68b5a-204">R</span></span>             | <span data-ttu-id="68b5a-205">R</span><span class="sxs-lookup"><span data-stu-id="68b5a-205">R</span></span>             | <span data-ttu-id="68b5a-206">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-206">1</span></span>            | <span data-ttu-id="68b5a-207">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-207">0.0</span></span>           |
| <span data-ttu-id="68b5a-208">\_ \_ mapa de píxeles \_ de GL G \_ a \_ g</span><span class="sxs-lookup"><span data-stu-id="68b5a-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="68b5a-209">G</span><span class="sxs-lookup"><span data-stu-id="68b5a-209">G</span></span>             | <span data-ttu-id="68b5a-210">G</span><span class="sxs-lookup"><span data-stu-id="68b5a-210">G</span></span>             | <span data-ttu-id="68b5a-211">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-211">1</span></span>            | <span data-ttu-id="68b5a-212">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-212">0.0</span></span>           |
| <span data-ttu-id="68b5a-213">\_ \_ mapa de píxeles \_ de contabilidad B \_ a \_ b</span><span class="sxs-lookup"><span data-stu-id="68b5a-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="68b5a-214">B</span><span class="sxs-lookup"><span data-stu-id="68b5a-214">B</span></span>             | <span data-ttu-id="68b5a-215">B</span><span class="sxs-lookup"><span data-stu-id="68b5a-215">B</span></span>             | <span data-ttu-id="68b5a-216">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-216">1</span></span>            | <span data-ttu-id="68b5a-217">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-217">0.0</span></span>           |
| <span data-ttu-id="68b5a-218">\_ \_ \_ la asignación de píxeles de GL \_ a a \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="68b5a-219">A</span><span class="sxs-lookup"><span data-stu-id="68b5a-219">A</span></span>             | <span data-ttu-id="68b5a-220">A</span><span class="sxs-lookup"><span data-stu-id="68b5a-220">A</span></span>             | <span data-ttu-id="68b5a-221">1</span><span class="sxs-lookup"><span data-stu-id="68b5a-221">1</span></span>            | <span data-ttu-id="68b5a-222">0,0</span><span class="sxs-lookup"><span data-stu-id="68b5a-222">0.0</span></span>           |



 

<span data-ttu-id="68b5a-223">Las siguientes funciones recuperan información relacionada con **glPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="68b5a-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="68b5a-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ \_ \_ \_ \_ el argumento de mapa de píxeles de contabilidad</span><span class="sxs-lookup"><span data-stu-id="68b5a-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="68b5a-225">**glGet** con el argumento de asignación de píxeles de contabilidad de argumentos \_ \_ \_ \_ a \_ \_ tamaño s</span><span class="sxs-lookup"><span data-stu-id="68b5a-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="68b5a-226">**glGet** con el argumento de mapa de píxeles de GL \_ \_ \_ I \_ a \_ tamaño de R \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="68b5a-227">**glGet** con el argumento de la asignación de píxeles de GL \_ \_ \_ I \_ a \_ G \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="68b5a-228">**glGet** con el argumento de mapa de píxeles de GL \_ \_ \_ I \_ a \_ B \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="68b5a-229">**glGet** con el argumento de \_ la asignación de píxeles de GL \_ \_ I \_ a \_ un \_ tamaño</span><span class="sxs-lookup"><span data-stu-id="68b5a-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="68b5a-230">**glGet** con el argumento de la asignación de píxeles de contabilidad \_ \_ \_ r \_ a \_ \_ tamaño r</span><span class="sxs-lookup"><span data-stu-id="68b5a-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="68b5a-231">**glGet** con el argumento de la asignación de píxeles de GL \_ \_ \_ G \_ a \_ g \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="68b5a-232">**glGet** con el tamaño de la asignación de píxeles de contabilidad de argumento \_ \_ \_ b \_ a \_ B \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="68b5a-233">**glGet** con el argumento GL de \_ píxel de \_ \_ la asignación \_ a a \_ un \_ tamaño</span><span class="sxs-lookup"><span data-stu-id="68b5a-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="68b5a-234">**glGet** con el argumento \_ \_ tabla de \_ mapa de píxeles máx. \_</span><span class="sxs-lookup"><span data-stu-id="68b5a-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="68b5a-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b5a-235">Requirements</span></span>



| <span data-ttu-id="68b5a-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b5a-236">Requirement</span></span> | <span data-ttu-id="68b5a-237">Value</span><span class="sxs-lookup"><span data-stu-id="68b5a-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b5a-238">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b5a-238">Minimum supported client</span></span><br/> | <span data-ttu-id="68b5a-239">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68b5a-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="68b5a-240">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b5a-240">Minimum supported server</span></span><br/> | <span data-ttu-id="68b5a-241">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68b5a-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68b5a-242">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68b5a-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b5a-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="68b5a-244">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68b5a-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="68b5a-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="68b5a-246">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68b5a-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68b5a-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b5a-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b5a-248">Vea también</span><span class="sxs-lookup"><span data-stu-id="68b5a-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b5a-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="68b5a-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="68b5a-250">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="68b5a-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="68b5a-251">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="68b5a-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="68b5a-252">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="68b5a-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="68b5a-253">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="68b5a-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="68b5a-254">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="68b5a-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="68b5a-255">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="68b5a-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="68b5a-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="68b5a-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="68b5a-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="68b5a-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





