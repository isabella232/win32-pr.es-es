---
description: Marcas que se pasan a la función TraceRay para invalidar la transparencia, la selección y el comportamiento de tiempo de espera.
ms.assetid: ''
title: Enumeración RAY_FLAG
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
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705343"
---
# <a name="ray_flag-enumeration"></a><span data-ttu-id="b8aa6-103">\_Enumeración de marca de rayo</span><span class="sxs-lookup"><span data-stu-id="b8aa6-103">RAY\_FLAG enumeration</span></span>

<span data-ttu-id="b8aa6-104">Marcas que se pasan a la función [**TraceRay**](traceray-function.md) para invalidar la transparencia, la selección y el comportamiento de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-104">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8aa6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8aa6-105">Syntax</span></span>


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a><span data-ttu-id="b8aa6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b8aa6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b8aa6-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**marca de rayo \_ \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-108">No hay opciones seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-108">No options selected.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa6-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**marca de rayo \_ \_ fuerza \_ opaca**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY\_FLAG\_FORCE\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-110">Todas las intersecciones de tipo primitivo de rayo encontradas en un raytrace se tratan como opacas.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-110">All ray-primitive intersections encountered in a raytrace are treated as opaque.</span></span>  <span data-ttu-id="b8aa6-111">Por tanto, no se ejecutará ningún sombreador de posicionamiento con independencia de si la geometría de aciertos especifica o no el \_ \_ indicador de geometría D3D12 RAYTRACING \_ \_ opaco y con independencia de las marcas de instancia de la instancia que se ha alcanzado.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-111">So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>

<span data-ttu-id="b8aa6-112">Esta marca se excluye mutuamente con la fuerza de la marca de rayo \_ \_ \_ no \_ opaca, el \_ marcador \_ de rayo y el \_ culling de marca de rayo \_ \_ \_ no \_ opacos.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-112">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_NON\_OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="b8aa6-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**fuerza de marcador de rayo \_ \_ \_ no \_ opaca**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY\_FLAG\_FORCE\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-114">Todas las intersecciones de tipo rayo-primitivo encontradas en un raytrace se tratan como no opacas.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-114">All ray-primitive intersections encountered in a raytrace are treated as non-opaque.</span></span>  <span data-ttu-id="b8aa6-115">Por lo tanto, cualquier sombreador de posicionamiento, si está presente, se ejecutará independientemente de si la geometría de aciertos especifica o no el \_ \_ indicador de geometría D3D12 RAYTRACING \_ \_ opaco y sin tener en consideración las marcas de instancia en la instancia que se alcanzó.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-115">So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>
<span data-ttu-id="b8aa6-116">Esta marca se excluye mutuamente con la \_ marca de rayo \_ FORCE_ \OPAQUE, el marcador de rayo \_ y el \_ \_ desecho de la marca de rayo \_ \_ \_ no \_ opacos.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-116">This flag is mutually exclusive with RAY\_FLAG\_FORCE_\OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="b8aa6-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_marca \_ de rayo aceptar \_ primer \_ acierto \_ y \_ finalizar \_ búsqueda**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY\_FLAG\_ACCEPT\_FIRST\_HIT\_AND\_END\_SEARCH**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-118">La primera intersección de rayo-primitivo encontrada en un raytrace hace que se llame automáticamente a **AcceptHitAndEndSearch** inmediatamente después de cualquier sombreador de posicionamiento, incluso si no hay ningún sombreador de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-118">The first ray-primitive intersection encountered in a raytrace automatically causes **AcceptHitAndEndSearch** to be called immediately after the any hit shader, including if there is no any hit shader.</span></span> 
 
<span data-ttu-id="b8aa6-119">La única excepción se produce cuando el anterior cualquier sombreador de posicionamiento llama a **IgnoreHit**, en cuyo caso el rayo continúa inalterado, de modo que el siguiente acierto se convierte en otro candidato como primer acierto.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-119">The only exception is when the preceding any hit shader calls **IgnoreHit**, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit.</span></span>  <span data-ttu-id="b8aa6-120">Para que se aplique esta excepción, se debe ejecutar realmente cualquier sombreador de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-120">For this exception to apply, the any hit shader has to actually be executed.</span></span>  <span data-ttu-id="b8aa6-121">Por lo tanto, si se omite cualquier sombreador de posicionamiento porque el acierto se trata como opaco (por ejemplo, debido a la marca de rayo \_ \_ Force \_ opaco o D3D12 RAYTRACING, el marcador de \_ \_ geometría \_ \_ opaco o D3D12 \_ RAYTRACING \_ \_ \_ se establece en opaca), se llama a **AcceptHitAndEndSearch** .</span><span class="sxs-lookup"><span data-stu-id="b8aa6-121">So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY\_FLAG\_FORCE\_OPAQUE or D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE or D3D12\_RAYTRACING\_INSTANCE\_FLAG\_OPAQUE being set), then **AcceptHitAndEndSearch** is called.</span></span>

<span data-ttu-id="b8aa6-122">Si un sombreador de posicionamiento más cercano está presente en el primer acierto, se invoca a menos que la marca de rayo \_ \_ omitir el \_ \_ sombreador de posicionamiento más cercano \_ también esté presente.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-122">If a closest hit shader is present at the first hit, it gets invoked unless RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER is also present.</span></span>  <span data-ttu-id="b8aa6-123">El golpe encontrado se considera "más cercano", aunque es posible que no se hayan visitado otros posibles aciertos que podrían estar más cerca del rayo.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-123">The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.</span></span>

<span data-ttu-id="b8aa6-124">Un uso típico de esta marca es para las sombras, donde solo es necesario encontrar un solo acierto.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-124">A typical use for this flag is for shadows, where only a single hit needs to be found.</span></span>


</dd> <dt>

<span data-ttu-id="b8aa6-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**marca de rayo \_ \_ omitir el \_ \_ sombreador de posicionamiento más cercano \_**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-126">Incluso si se ha confirmado al menos una visita y el grupo de aciertos para el acierto más cercano contiene un sombreador de posicionamiento más cercano, omitirá la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-126">Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.</span></span> 

</dd> <dt>

<span data-ttu-id="b8aa6-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**\_marcador de \_ rayo \_ hacia atrás con \_ \_ triángulos**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-128">Habilita la selección de triángulos hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-128">Enables culling of back facing triangles.</span></span> <span data-ttu-id="b8aa6-129">Consulte **D3D12 \_ RAYTRACING \_ Instance \_ Flags** para seleccionar qué triángulos van a la inversa, por instancia.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-129">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="b8aa6-130">En las instancias de que especifican \_ \_ la marca de instancia de D3D12 RAYTRACING \_ \_ \_ \_ deshabilitada, esta marca no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-130">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="b8aa6-131">En los tipos de geometría distintos de los \_ \_ triángulos del tipo de geometría D3D12 RAYTRACING \_ \_ , esta marca no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-131">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="b8aa6-132">Esta marca se excluye mutuamente con \_ \_ \_ \_ triángulos frontales de selección de marca de rayo \_ .</span><span class="sxs-lookup"><span data-stu-id="b8aa6-132">This flag is mutually exclusive with RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="b8aa6-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**\_ \_ \_ triángulos frontales de selección \_ de marca \_ de rayo**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-134">Habilita la selección de triángulos de cara frontal.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-134">Enables culling of front facing triangles.</span></span> <span data-ttu-id="b8aa6-135">Consulte **D3D12 \_ RAYTRACING \_ Instance \_ Flags** para seleccionar qué triángulos van a la inversa, por instancia.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-135">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="b8aa6-136">En las instancias de que especifican \_ \_ la marca de instancia de D3D12 RAYTRACING \_ \_ \_ \_ deshabilitada, esta marca no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-136">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="b8aa6-137">En los tipos de geometría distintos de los \_ \_ triángulos del tipo de geometría D3D12 RAYTRACING \_ \_ , esta marca no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-137">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="b8aa6-138">Este marcador es mutuamente excluyente con \_ \_ \_ \_ triángulos de selección de marca de rayo \_ .</span><span class="sxs-lookup"><span data-stu-id="b8aa6-138">This flag is mutually exclusive with RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="b8aa6-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**marcador de rayo de \_ \_ selección \_ opaca**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY\_FLAG\_CULL\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-140">Selecciona todos los primitivos que se consideran opacos en función de sus marcas de geometría e instancia.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-140">Culls all primitives that are considered opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="b8aa6-141">Esta marca se excluye mutuamente con la \_ marca de rayo \_ Force \_ opaco, la fuerza de la marca de rayo \_ \_ \_ no \_ opaca y la marca de rayo \_ \_ \_ no \_ opaca.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-141">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="b8aa6-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**selección de marca de rayo \_ \_ \_ no \_ opaca**</span><span class="sxs-lookup"><span data-stu-id="b8aa6-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY\_FLAG\_CULL\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="b8aa6-143">Selecciona todos los primitivos que se consideran no opacos en función de sus marcas de geometría e instancia.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-143">Culls all primitives that are considered non-opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="b8aa6-144">Esta marca se excluye mutuamente con la \_ marca de rayo \_ Force \_ opaco, la fuerza de la marca de rayo \_ \_ \_ no \_ opaca y la de marcador de rayo \_ \_ \_ opaca.</span><span class="sxs-lookup"><span data-stu-id="b8aa6-144">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_OPAQUE.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="b8aa6-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8aa6-145">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="b8aa6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8aa6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8aa6-147">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="b8aa6-147">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




