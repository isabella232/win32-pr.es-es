---
description: Identifica el tipo de consulta.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumeración D3DQUERYTYPE (D3D9Types.h)
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
ms.openlocfilehash: 7a9c20050e7d0dce5a19664d937c016a475a9a13
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343080"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="559eb-103">D3DQUERYTYPE (enumeración)</span><span class="sxs-lookup"><span data-stu-id="559eb-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="559eb-104">Identifica el tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="559eb-104">Identifies the query type.</span></span> <span data-ttu-id="559eb-105">Para obtener información sobre las consultas, vea [Consultas (Direct3D 9)](queries.md)</span><span class="sxs-lookup"><span data-stu-id="559eb-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="559eb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="559eb-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="559eb-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="559eb-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="559eb-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="559eb-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-109">Consulta de sugerencias de controlador sobre el diseño de datos para el almacenamiento en caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="559eb-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="559eb-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-111">Consulte el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="559eb-111">Query the resource manager.</span></span> <span data-ttu-id="559eb-112">Para esta consulta, las marcas de comportamiento del dispositivo deben incluir [D3DCREATE \_ DISABLE \_ DRIVER \_ MANAGEMENT](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="559eb-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="559eb-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="559eb-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-114">Consultar estadísticas de vértices.</span><span class="sxs-lookup"><span data-stu-id="559eb-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**EVENTO D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="559eb-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-116">Consulte todos y cada uno de los eventos asincrónicos emitidos desde llamadas API.</span><span class="sxs-lookup"><span data-stu-id="559eb-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**OCLUSIÓN DE D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="559eb-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-118">Una consulta de oclusión devuelve el número de píxeles que pasan las pruebas z.</span><span class="sxs-lookup"><span data-stu-id="559eb-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="559eb-119">Estos píxeles son para los primitivos dibujados entre el problema [**de D3DISSUE \_ BEGIN**](d3dissue-begin.md) y [**D3DISSUE \_ END.**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="559eb-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="559eb-120">Esto permite que una aplicación compruebe el resultado de la oclusión en 0.</span><span class="sxs-lookup"><span data-stu-id="559eb-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="559eb-121">Cero está totalmente ocluido, lo que significa que los píxeles no son visibles desde la posición actual de la cámara.</span><span class="sxs-lookup"><span data-stu-id="559eb-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**MARCA DE TIEMPO D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="559eb-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-123">Devuelve una marca de tiempo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="559eb-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="559eb-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-125">Use esta consulta para notificar a una aplicación si la frecuencia del contador ha cambiado desde D3DQUERYTYPE \_ TIMESTAMP.</span><span class="sxs-lookup"><span data-stu-id="559eb-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="559eb-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-127">Este resultado de consulta es **TRUE** si no se puede garantizar que los valores de las consultas TIMESTAMP de D3DQUERYTYPE sean continuos a lo largo de la duración de la consulta \_ D3DQUERYTYPE \_ TIMESTAMPDISJOINT.</span><span class="sxs-lookup"><span data-stu-id="559eb-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="559eb-128">De lo contrario, el resultado de la **consulta es FALSE.**</span><span class="sxs-lookup"><span data-stu-id="559eb-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="559eb-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-130">Porcentaje de tiempo de procesamiento de datos de canalización.</span><span class="sxs-lookup"><span data-stu-id="559eb-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**INTERFAZ \_ D3DQUERYTYPETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="559eb-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-132">Porcentaje de tiempo de procesamiento de datos en el controlador.</span><span class="sxs-lookup"><span data-stu-id="559eb-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**VÉRTICES \_ D3DQUERYTYPETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="559eb-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-134">Porcentaje de tiempo de procesamiento de datos del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="559eb-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="559eb-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-136">Porcentaje de tiempo de procesamiento de datos del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="559eb-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="559eb-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-138">Comparaciones de medidas de rendimiento para ayudar a comprender el rendimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="559eb-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="559eb-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-140">Mida el rendimiento de la tasa de aciertos de caché para texturas y vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="559eb-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="559eb-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="559eb-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="559eb-142">Eficiencia de la asignación de memoria contenida en una [**estructura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)</span><span class="sxs-lookup"><span data-stu-id="559eb-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

<span data-ttu-id="559eb-143">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="559eb-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="559eb-144">D3DQUERYTYPE MEMORYPRESSURE solo está disponible en Direct3D9Ex que se ejecuta \_ en Windows 7 (o en un sistema operativo más actual).</span><span class="sxs-lookup"><span data-stu-id="559eb-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="559eb-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="559eb-145">Requirements</span></span>



| <span data-ttu-id="559eb-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="559eb-146">Requirement</span></span> | <span data-ttu-id="559eb-147">Value</span><span class="sxs-lookup"><span data-stu-id="559eb-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="559eb-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="559eb-148">Header</span></span><br/> | <dl> <span data-ttu-id="559eb-149"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="559eb-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="559eb-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="559eb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="559eb-151">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="559eb-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="559eb-152">**IDirect3DDevice9::CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="559eb-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
