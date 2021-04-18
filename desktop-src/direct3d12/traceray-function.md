---
description: Envía un rayo en una búsqueda de aciertos en una estructura de aceleración.
ms.assetid: ''
title: Función TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105707573"
---
# <a name="traceray-function"></a><span data-ttu-id="a95a9-103">Función TraceRay</span><span class="sxs-lookup"><span data-stu-id="a95a9-103">TraceRay function</span></span>

<span data-ttu-id="a95a9-104">Envía un rayo en una búsqueda de aciertos en una estructura de aceleración.</span><span class="sxs-lookup"><span data-stu-id="a95a9-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a95a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a95a9-105">Syntax</span></span>
<span data-ttu-id="a95a9-106">Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:</span><span class="sxs-lookup"><span data-stu-id="a95a9-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="a95a9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a95a9-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="a95a9-108">Estructura de aceleración de nivel superior que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a95a9-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="a95a9-109">Si se especifica una estructura de aceleración nula, se fuerza una pérdida.</span><span class="sxs-lookup"><span data-stu-id="a95a9-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="a95a9-110">Combinación válida de valores de [ray_flag](ray_flag.md) .</span><span class="sxs-lookup"><span data-stu-id="a95a9-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="a95a9-111">El sistema solo propaga las marcas de rayo definidas, es decir, que están visibles para el intrínseco del sombreador [RayFlags](rayflags.md) .</span><span class="sxs-lookup"><span data-stu-id="a95a9-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="a95a9-112">Entero sin signo, los 8 bits inferiores de los cuales se usan para incluir o rechazar instancias de Geometry basadas en InstanceMask en cada instancia.</span><span class="sxs-lookup"><span data-stu-id="a95a9-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="a95a9-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a95a9-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="a95a9-114">Entero sin signo que especifica el desplazamiento que se va a agregar en los cálculos de direccionamiento dentro de las tablas de sombreador para la indización del grupo de visitas.</span><span class="sxs-lookup"><span data-stu-id="a95a9-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="a95a9-115">Solo se usan los cuatro bits inferiores de este valor.</span><span class="sxs-lookup"><span data-stu-id="a95a9-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="a95a9-116">Entero sin signo que especifica el intervalo que se va a multiplicar por *GeometryContributionToHitGroupIndex*, que es solo el índice de base 0 que la aplicación proporcionó la geometría en la estructura de aceleración de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a95a9-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="a95a9-117">Solo se usan los 16 bits inferiores de este valor de multiplicador.</span><span class="sxs-lookup"><span data-stu-id="a95a9-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="a95a9-118">Entero sin signo que especifica el índice del sombreador de errores dentro de una tabla de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a95a9-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="a95a9-119">[**RayDesc**](raydesc.md) que representa el rayo del que se va a realizar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="a95a9-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="a95a9-120">Una carga de rayo definida por el usuario a la que se tiene acceso tanto para la entrada como para la salida mediante sombreadores invocados durante raytracing.</span><span class="sxs-lookup"><span data-stu-id="a95a9-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="a95a9-121">Una vez finalizado [**TraceRay**](traceray-function.md) , el llamador puede tener acceso también a la carga.</span><span class="sxs-lookup"><span data-stu-id="a95a9-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="a95a9-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a95a9-122">Return Value</span></span>

<span data-ttu-id="a95a9-123">**void**</span><span class="sxs-lookup"><span data-stu-id="a95a9-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="a95a9-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a95a9-124">Remarks</span></span>

<span data-ttu-id="a95a9-125">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="a95a9-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="a95a9-126">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="a95a9-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="a95a9-127">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="a95a9-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="a95a9-128">**Sombreador de generación de rayos**</span><span class="sxs-lookup"><span data-stu-id="a95a9-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="a95a9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a95a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95a9-130">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="a95a9-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




