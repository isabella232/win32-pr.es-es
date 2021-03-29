---
title: función glPolygonMode (GL. h)
description: La función glPolygonMode selecciona un modo de rasterización de polígono.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode (función) OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666081"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="a9134-104">glPolygonMode función)</span><span class="sxs-lookup"><span data-stu-id="a9134-104">glPolygonMode function</span></span>

<span data-ttu-id="a9134-105">La función **glPolygonMode** selecciona un modo de rasterización de polígono.</span><span class="sxs-lookup"><span data-stu-id="a9134-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9134-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9134-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="a9134-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9134-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9134-108">*Portada*</span><span class="sxs-lookup"><span data-stu-id="a9134-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="a9134-109">Polígonos a los que se aplica el *modo* .</span><span class="sxs-lookup"><span data-stu-id="a9134-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="a9134-110">Debe estar \_ en la parte frontal de los polígonos frontales, en el libro \_ de reserva para los polígonos de respaldo, o en la \_ parte frontal \_ y \_ posterior para los polígonos frontal y trasero.</span><span class="sxs-lookup"><span data-stu-id="a9134-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="a9134-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="a9134-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="a9134-112">La forma en que se rasterizarán los polígonos.</span><span class="sxs-lookup"><span data-stu-id="a9134-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="a9134-113">Se definen los siguientes modos y se pueden especificar en el *modo*.</span><span class="sxs-lookup"><span data-stu-id="a9134-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="a9134-114">El valor predeterminado es el \_ relleno de contabilidad para los polígonos delante y detrás.</span><span class="sxs-lookup"><span data-stu-id="a9134-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="a9134-115">Value</span><span class="sxs-lookup"><span data-stu-id="a9134-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="a9134-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a9134-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="a9134-117"><dt>**punto de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="a9134-118">Los vértices de polígono que se marcan como el inicio de un borde del límite se dibujan como puntos.</span><span class="sxs-lookup"><span data-stu-id="a9134-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="a9134-119">Los atributos de punto, como el \_ \_ tamaño de los puntos de la contabilidad y \_ \_ el punto de contabilidad suavizado controlan la rasterización de los puntos.</span><span class="sxs-lookup"><span data-stu-id="a9134-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="a9134-120">Los atributos de rasterización de polígono distintos del modo de polígono de contabilidad \_ \_ no tienen ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="a9134-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="a9134-121"><dt>**línea de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="a9134-122">Los bordes de los límites del polígono se dibujan como segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="a9134-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="a9134-123">Se tratan como segmentos de línea conectados para el punteado de línea; el contador y el patrón punteado de línea no se restablecen entre segmentos (vea [**glLineStipple**](gllinestipple.md)).</span><span class="sxs-lookup"><span data-stu-id="a9134-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="a9134-124">Los atributos de línea como \_ \_ el ancho de línea de libro de contabilidad y \_ \_ el control suavizado de línea de contabilidad controlan la rasterización de las líneas.</span><span class="sxs-lookup"><span data-stu-id="a9134-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="a9134-125">Los atributos de rasterización de polígono distintos del modo de polígono de contabilidad \_ \_ no tienen ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="a9134-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="a9134-126"><dt>**relleno de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="a9134-127">El interior del polígono se rellena.</span><span class="sxs-lookup"><span data-stu-id="a9134-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="a9134-128">Los atributos Polygon, como GL \_ Polygon \_ punteate y GL \_ poligonal \_ controlan la rasterización del polígono.</span><span class="sxs-lookup"><span data-stu-id="a9134-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9134-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9134-129">Return value</span></span>

<span data-ttu-id="a9134-130">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a9134-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9134-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a9134-131">Error codes</span></span>

<span data-ttu-id="a9134-132">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a9134-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a9134-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="a9134-133">Name</span></span>                                                                                                  | <span data-ttu-id="a9134-134">Significado</span><span class="sxs-lookup"><span data-stu-id="a9134-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9134-135"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a9134-136">Cualquier *esfera* o *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="a9134-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="a9134-137"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a9134-138">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a9134-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a9134-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9134-139">Remarks</span></span>

<span data-ttu-id="a9134-140">La función **glPolygonMode** controla la interpretación de polígonos para la rasterización.</span><span class="sxs-lookup"><span data-stu-id="a9134-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="a9134-141">El parámetro *facial* describe el *modo* de polígonos que se aplica a: polígonos frontales ( \_ front-end), polígonos de orientación hacia atrás ( \_ retroceder) o ambos (de la \_ parte frontal \_ y \_ posterior).</span><span class="sxs-lookup"><span data-stu-id="a9134-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="a9134-142">El modo de polígono afecta solo a la rasterización final de los polígonos.</span><span class="sxs-lookup"><span data-stu-id="a9134-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="a9134-143">En concreto, los vértices de un polígono están iluminados y el polígono se recorta y, posiblemente, se selecciona antes de que se apliquen estos modos.</span><span class="sxs-lookup"><span data-stu-id="a9134-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="a9134-144">Para dibujar una superficie con polígonos de orientación hacia atrás rellenados y polígonos de cara frontal detallados, llame a</span><span class="sxs-lookup"><span data-stu-id="a9134-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="a9134-145">**glPolygonMode**(libro \_ frontal, línea de contabilidad \_ );</span><span class="sxs-lookup"><span data-stu-id="a9134-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="a9134-146">Los vértices se marcan como límite o no límite con una marca de borde.</span><span class="sxs-lookup"><span data-stu-id="a9134-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="a9134-147">OpenGL genera internamente marcas de borde cuando descompone polígonos y se pueden establecer explícitamente mediante [**glEdgeFlag**](gledgeflag-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a9134-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="a9134-148">La siguiente función recupera información relacionada con **glPolygonMode**:</span><span class="sxs-lookup"><span data-stu-id="a9134-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="a9134-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de polígono de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="a9134-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="a9134-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9134-150">Requirements</span></span>



| <span data-ttu-id="a9134-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9134-151">Requirement</span></span> | <span data-ttu-id="a9134-152">Value</span><span class="sxs-lookup"><span data-stu-id="a9134-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9134-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9134-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a9134-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a9134-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a9134-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9134-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a9134-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9134-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9134-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9134-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9134-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a9134-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9134-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9134-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9134-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9134-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9134-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9134-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9134-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9134-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9134-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a9134-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a9134-165">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a9134-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a9134-166">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a9134-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a9134-167">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="a9134-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="a9134-168">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="a9134-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="a9134-169">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="a9134-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="a9134-170">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="a9134-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





