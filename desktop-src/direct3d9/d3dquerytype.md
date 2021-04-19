---
description: Identifica el tipo de consulta.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumeración D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707928"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="7d962-103">Enumeración D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="7d962-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="7d962-104">Identifica el tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="7d962-104">Identifies the query type.</span></span> <span data-ttu-id="7d962-105">Para obtener información sobre las consultas, vea [consultas (Direct3D 9)](queries.md)</span><span class="sxs-lookup"><span data-stu-id="7d962-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d962-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d962-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="7d962-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="7d962-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d962-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="7d962-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-109">Consultar Sugerencias de controladores sobre el diseño de datos para el almacenamiento en caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="7d962-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="7d962-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-111">Consulte el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d962-111">Query the resource manager.</span></span> <span data-ttu-id="7d962-112">En esta consulta, las marcas de comportamiento del dispositivo deben incluir [D3DCREATE \_ deshabilitar la \_ \_ Administración de controladores](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="7d962-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d962-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="7d962-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-114">Estadísticas de vértices de consulta.</span><span class="sxs-lookup"><span data-stu-id="7d962-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Evento D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="7d962-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-116">Consultar todos los eventos asincrónicos que se han emitido desde llamadas API.</span><span class="sxs-lookup"><span data-stu-id="7d962-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**Oclusión de D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="7d962-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-118">Una consulta de oclusión devuelve el número de píxeles que superan la prueba z.</span><span class="sxs-lookup"><span data-stu-id="7d962-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="7d962-119">Estos píxeles son para las primitivas dibujadas entre el problema de [**D3DISSUE \_ Begin**](d3dissue-begin.md) y [**D3DISSUE \_ End**](d3dissue-end.md).</span><span class="sxs-lookup"><span data-stu-id="7d962-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="7d962-120">Esto permite que una aplicación Compruebe el resultado de la oclusión en 0.</span><span class="sxs-lookup"><span data-stu-id="7d962-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="7d962-121">Cero es totalmente ocluidos, lo que significa que los píxeles no son visibles desde la posición de la cámara actual.</span><span class="sxs-lookup"><span data-stu-id="7d962-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**Marca de tiempo D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="7d962-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-123">Devuelve una marca de tiempo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7d962-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="7d962-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-125">Use esta consulta para notificar a una aplicación si la frecuencia del contador ha cambiado desde la marca de tiempo D3DQUERYTYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="7d962-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="7d962-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-127">Este resultado de la consulta es **true** si no se puede garantizar que los valores de las consultas de marca de tiempo de D3DQUERYTYPE \_ sean continuos a lo largo de la duración de la \_ consulta D3DQUERYTYPE TIMESTAMPDISJOINT.</span><span class="sxs-lookup"><span data-stu-id="7d962-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="7d962-128">De lo contrario, el resultado de la consulta es **false**.</span><span class="sxs-lookup"><span data-stu-id="7d962-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="7d962-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-130">Porcentaje de tiempo de procesamiento de datos de canalización.</span><span class="sxs-lookup"><span data-stu-id="7d962-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="7d962-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-132">Porcentaje de tiempo de procesamiento de datos en el controlador.</span><span class="sxs-lookup"><span data-stu-id="7d962-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="7d962-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-134">Porcentaje de tiempo que procesa los datos del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="7d962-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="7d962-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-136">Porcentaje de tiempo de procesamiento de datos del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="7d962-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="7d962-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-138">Comparaciones de medición del rendimiento para ayudar a comprender el rendimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7d962-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="7d962-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-140">Mida el rendimiento de la tasa de aciertos de caché para las texturas y los vértices indizados.</span><span class="sxs-lookup"><span data-stu-id="7d962-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="7d962-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="7d962-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="7d962-142">Eficiencia de la asignación de memoria contenida en una estructura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="7d962-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d962-143">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="7d962-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d962-144">D3DQUERYTYPE \_ MEMORYPRESSURE solo está disponible en Direct3D9Ex que se ejecuta en Windows 7 (o en el sistema operativo actual).</span><span class="sxs-lookup"><span data-stu-id="7d962-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d962-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d962-145">Requirements</span></span>



| <span data-ttu-id="7d962-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d962-146">Requirement</span></span> | <span data-ttu-id="7d962-147">Value</span><span class="sxs-lookup"><span data-stu-id="7d962-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d962-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d962-148">Header</span></span><br/> | <dl> <span data-ttu-id="7d962-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d962-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d962-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d962-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d962-151">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7d962-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="7d962-152">**IDirect3DDevice9:: CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="7d962-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
