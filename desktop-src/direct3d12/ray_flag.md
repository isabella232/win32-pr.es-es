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
# <a name="ray_flag-enumeration"></a>\_Enumeración de marca de rayo

Marcas que se pasan a la función [**TraceRay**](traceray-function.md) para invalidar la transparencia, la selección y el comportamiento de tiempo de espera.

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**marca de rayo \_ \_ ninguno**
</dt> <dd>

No hay opciones seleccionadas.

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**marca de rayo \_ \_ fuerza \_ opaca**
</dt> <dd>

Todas las intersecciones de tipo primitivo de rayo encontradas en un raytrace se tratan como opacas.  Por tanto, no se ejecutará ningún sombreador de posicionamiento con independencia de si la geometría de aciertos especifica o no el \_ \_ indicador de geometría D3D12 RAYTRACING \_ \_ opaco y con independencia de las marcas de instancia de la instancia que se ha alcanzado.

Esta marca se excluye mutuamente con la fuerza de la marca de rayo \_ \_ \_ no \_ opaca, el \_ marcador \_ de rayo y el \_ culling de marca de rayo \_ \_ \_ no \_ opacos.


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**fuerza de marcador de rayo \_ \_ \_ no \_ opaca**
</dt> <dd>

Todas las intersecciones de tipo rayo-primitivo encontradas en un raytrace se tratan como no opacas.  Por lo tanto, cualquier sombreador de posicionamiento, si está presente, se ejecutará independientemente de si la geometría de aciertos especifica o no el \_ \_ indicador de geometría D3D12 RAYTRACING \_ \_ opaco y sin tener en consideración las marcas de instancia en la instancia que se alcanzó.
Esta marca se excluye mutuamente con la \_ marca de rayo \_ FORCE_ \OPAQUE, el marcador de rayo \_ y el \_ \_ desecho de la marca de rayo \_ \_ \_ no \_ opacos.


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_marca \_ de rayo aceptar \_ primer \_ acierto \_ y \_ finalizar \_ búsqueda**
</dt> <dd>

La primera intersección de rayo-primitivo encontrada en un raytrace hace que se llame automáticamente a **AcceptHitAndEndSearch** inmediatamente después de cualquier sombreador de posicionamiento, incluso si no hay ningún sombreador de posicionamiento. 
 
La única excepción se produce cuando el anterior cualquier sombreador de posicionamiento llama a **IgnoreHit**, en cuyo caso el rayo continúa inalterado, de modo que el siguiente acierto se convierte en otro candidato como primer acierto.  Para que se aplique esta excepción, se debe ejecutar realmente cualquier sombreador de posicionamiento.  Por lo tanto, si se omite cualquier sombreador de posicionamiento porque el acierto se trata como opaco (por ejemplo, debido a la marca de rayo \_ \_ Force \_ opaco o D3D12 RAYTRACING, el marcador de \_ \_ geometría \_ \_ opaco o D3D12 \_ RAYTRACING \_ \_ \_ se establece en opaca), se llama a **AcceptHitAndEndSearch** .

Si un sombreador de posicionamiento más cercano está presente en el primer acierto, se invoca a menos que la marca de rayo \_ \_ omitir el \_ \_ sombreador de posicionamiento más cercano \_ también esté presente.  El golpe encontrado se considera "más cercano", aunque es posible que no se hayan visitado otros posibles aciertos que podrían estar más cerca del rayo.

Un uso típico de esta marca es para las sombras, donde solo es necesario encontrar un solo acierto.


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**marca de rayo \_ \_ omitir el \_ \_ sombreador de posicionamiento más cercano \_**
</dt> <dd>

Incluso si se ha confirmado al menos una visita y el grupo de aciertos para el acierto más cercano contiene un sombreador de posicionamiento más cercano, omitirá la ejecución de ese sombreador. 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**\_marcador de \_ rayo \_ hacia atrás con \_ \_ triángulos**
</dt> <dd>

Habilita la selección de triángulos hacia atrás. Consulte **D3D12 \_ RAYTRACING \_ Instance \_ Flags** para seleccionar qué triángulos van a la inversa, por instancia.

En las instancias de que especifican \_ \_ la marca de instancia de D3D12 RAYTRACING \_ \_ \_ \_ deshabilitada, esta marca no tiene ningún efecto.

En los tipos de geometría distintos de los \_ \_ triángulos del tipo de geometría D3D12 RAYTRACING \_ \_ , esta marca no tiene ningún efecto.

Esta marca se excluye mutuamente con \_ \_ \_ \_ triángulos frontales de selección de marca de rayo \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**\_ \_ \_ triángulos frontales de selección \_ de marca \_ de rayo**
</dt> <dd>

Habilita la selección de triángulos de cara frontal. Consulte **D3D12 \_ RAYTRACING \_ Instance \_ Flags** para seleccionar qué triángulos van a la inversa, por instancia.

En las instancias de que especifican \_ \_ la marca de instancia de D3D12 RAYTRACING \_ \_ \_ \_ deshabilitada, esta marca no tiene ningún efecto.

En los tipos de geometría distintos de los \_ \_ triángulos del tipo de geometría D3D12 RAYTRACING \_ \_ , esta marca no tiene ningún efecto.

Este marcador es mutuamente excluyente con \_ \_ \_ \_ triángulos de selección de marca de rayo \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**marcador de rayo de \_ \_ selección \_ opaca**
</dt> <dd>

Selecciona todos los primitivos que se consideran opacos en función de sus marcas de geometría e instancia.

Esta marca se excluye mutuamente con la \_ marca de rayo \_ Force \_ opaco, la fuerza de la marca de rayo \_ \_ \_ no \_ opaca y la marca de rayo \_ \_ \_ no \_ opaca.


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**selección de marca de rayo \_ \_ \_ no \_ opaca**
</dt> <dd>

Selecciona todos los primitivos que se consideran no opacos en función de sus marcas de geometría e instancia.

Esta marca se excluye mutuamente con la \_ marca de rayo \_ Force \_ opaco, la fuerza de la marca de rayo \_ \_ \_ no \_ opaca y la de marcador de rayo \_ \_ \_ opaca.


</dd>

## <a name="requirements"></a>Requisitos



## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




