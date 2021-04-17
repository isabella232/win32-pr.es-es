---
description: Se pasa a la función TraceRay para definir el origen, la dirección y las extensiones del rayo.
ms.assetid: ''
title: Estructura RayDesc
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705342"
---
# <a name="raydesc-structure"></a><span data-ttu-id="44f4c-103">Estructura RayDesc</span><span class="sxs-lookup"><span data-stu-id="44f4c-103">RayDesc structure</span></span>

<span data-ttu-id="44f4c-104">Se pasa a la función [**TraceRay**](traceray-function.md) para definir el origen, la dirección y las extensiones del rayo.</span><span class="sxs-lookup"><span data-stu-id="44f4c-104">Passed to the [**TraceRay**](traceray-function.md) function to define the origin, direction, and extents of the ray.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f4c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44f4c-105">Syntax</span></span>


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a><span data-ttu-id="44f4c-106">Campos</span><span class="sxs-lookup"><span data-stu-id="44f4c-106">Fields</span></span>

<dl> <dt>

<span data-ttu-id="44f4c-107"><span id="Origin"></span><span id="origin"></span>**Pescado**</span><span class="sxs-lookup"><span data-stu-id="44f4c-107"><span id="Origin"></span><span id="origin"></span>**Origin**</span></span>
</dt> <dd>

<span data-ttu-id="44f4c-108">El origen del rayo.</span><span class="sxs-lookup"><span data-stu-id="44f4c-108">The origin of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="44f4c-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span><span class="sxs-lookup"><span data-stu-id="44f4c-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span></span>
</dt> <dd>

<span data-ttu-id="44f4c-110">La extensión mínima del rayo.</span><span class="sxs-lookup"><span data-stu-id="44f4c-110">The minimum extent of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="44f4c-111"><span id="Direction"></span><span id="direction"></span>**Direcciona**</span><span class="sxs-lookup"><span data-stu-id="44f4c-111"><span id="Direction"></span><span id="direction"></span>**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="44f4c-112">Dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="44f4c-112">The direction of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="44f4c-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span><span class="sxs-lookup"><span data-stu-id="44f4c-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span></span>
</dt> <dd>

<span data-ttu-id="44f4c-114">La extensión máxima del rayo.</span><span class="sxs-lookup"><span data-stu-id="44f4c-114">The maximum extent of the ray.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="44f4c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44f4c-115">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="44f4c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="44f4c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f4c-117">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="44f4c-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




