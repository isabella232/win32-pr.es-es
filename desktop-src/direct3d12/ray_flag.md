---
description: Marcas que se pasan a la función TraceRay para invalidar la transparencia, la selección y el comportamiento de salida anticipada.
ms.assetid: ''
title: RAY_FLAG enumeración
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072910"
---
# <a name="ray_flag-enumeration"></a>Enumeración \_ RAY FLAG

Marcas que se pasan a la [**función TraceRay**](traceray-function.md) para invalidar la transparencia, la selección y el comportamiento de salida anticipada.

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

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY \_ FLAG \_ NONE**
</dt> <dd>

Ninguna opción seleccionada.

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY \_ FLAG \_ FORCE \_ OPAQUE**
</dt> <dd>

Todas las intersecciones primitivas de rayos encontradas en un raytrace se tratan como opacas.  Por lo tanto, no se ejecutará ningún sombreador de acceso independientemente de si la geometría de acceso especifica D3D12 RAYTRACING GEOMETRY FLAG OPAQUE e independientemente de las marcas de instancia de la instancia que se ha \_ \_ \_ \_ alcanzado.

Esta marca es mutuamente excluyente con RAY \_ FLAG \_ FORCE NON \_ \_ OPAQUE, RAY FLAG CULL OPAQUE y RAY \_ FLAG \_ \_ \_ \_ CULL \_ NON \_ OPAQUE.


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY \_ FLAG \_ FORCE \_ NON \_ OPAQUE**
</dt> <dd>

Todas las intersecciones primitivas de rayos encontradas en un raytrace se tratan como no opacas.  Por lo tanto, los sombreadores de impacto, si están presentes, se ejecutarán independientemente de si la geometría de acceso especifica D3D12 RAYTRACING GEOMETRY FLAG OPAQUE e independientemente de las marcas de instancia de la instancia que se ha \_ \_ \_ \_ alcanzado.
Esta marca es mutuamente excluyente con RAY \_ FLAG \_ FORCE_\OPAQUE, RAY FLAG CULL OPAQUE y \_ RAY FLAG \_ \_ \_ \_ CULL NON \_ \_ OPAQUE.


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY \_ FLAG \_ ACCEPT \_ FIRST \_ HIT \_ AND \_ END \_ SEARCH**
</dt> <dd>

La primera intersección entre rayos y primitivos encontrada en un raytrace hace que se llame automáticamente a **AcceptHitAndEndSearch** inmediatamente después de cualquier sombreador de llamadas, incluido si no hay ningún sombreador de llamadas. 
 
La única excepción es cuando el sombreador de llamadas anterior llama a **IgnoreHit**, en cuyo caso el rayo sigue sin ser afectado, de modo que el siguiente impacto se convierte en otro candidato para ser el primer impacto.  Para que se aplique esta excepción, se debe ejecutar realmente cualquier sombreador de pulsaciones.  Por lo tanto, si se omite cualquier sombreador de llamadas porque la operación se trata como opaca (por ejemplo, debido a que se establece RAY FLAG FORCE OPAQUE o \_ \_ \_ D3D12 \_ RAYTRACING GEOMETRY FLAG OPAQUE o \_ \_ \_ D3D12 RAYTRACING INSTANCE FLAG OPAQUE), se llama a \_ \_ \_ \_ **AcceptHitAndEndSearch.**

Si hay un sombreador de impacto más cercano en el primer hit, se invoca a menos que RAY \_ FLAG \_ SKIP \_ CLOSEST HIT SHADER también esté \_ \_ presente.  El único acierto que se encontró se considera "más cercano", aunque es posible que no se hayan visitado otros posibles aciertos que podrían estar más cerca del rayo.

Un uso típico de esta marca es para las sombras, donde solo es necesario encontrar una sola pulsación.


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY \_ FLAG \_ SKIP \_ CLOSEST \_ HIT \_ SHADER**
</dt> <dd>

Incluso si se ha confirmado al menos una pulsación y el grupo de pulsaciones para la pulsación más cercana contiene un sombreador de impacto más cercano, omita la ejecución de ese sombreador. 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**TRIÁNGULOS DE CULL DE LA MARCA RAY \_ \_ HACIA \_ \_ \_ ATRÁS**
</dt> <dd>

Habilita la selección de triángulos orientados hacia atrás. Consulte **D3D12 \_ RAYTRACING \_ INSTANCE \_ FLAGS** (MARCAS DE INSTANCIA DE RAYTRACING) para seleccionar qué triángulos están orientados hacia atrás, por instancia.

En las instancias que especifican D3D12 \_ RAYTRACING \_ INSTANCE FLAG TRIANGLE \_ \_ \_ CULL \_ DISABLE, esta marca no tiene ningún efecto.

En tipos de geometría distintos de D3D12 \_ RAYTRACING \_ GEOMETRY \_ TYPE \_ TRIANGLES, esta marca no tiene ningún efecto.

Esta marca es mutuamente excluyente con RAY \_ FLAG \_ CULL \_ FRONT FACING \_ \_ TRIANGLES.


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**TRIÁNGULOS \_ FRONTALES \_ DE CULL DE LA MARCA \_ \_ \_ RAY**
</dt> <dd>

Habilita la selección de triángulos frontales. Consulte **D3D12 \_ RAYTRACING \_ INSTANCE \_ FLAGS** (MARCAS DE INSTANCIA DE RAYTRACING) para seleccionar qué triángulos están orientados hacia atrás, por instancia.

En las instancias que especifican D3D12 \_ RAYTRACING \_ INSTANCE FLAG TRIANGLE \_ \_ \_ CULL \_ DISABLE, esta marca no tiene ningún efecto.

En tipos de geometría distintos de D3D12 \_ RAYTRACING \_ GEOMETRY \_ TYPE \_ TRIANGLES, esta marca no tiene ningún efecto.

Esta marca es mutuamente excluyente con RAY \_ FLAG \_ CULL \_ BACK FACING \_ \_ TRIANGLES.


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY \_ FLAG \_ CULL \_ OPAQUE**
</dt> <dd>

Anula todas las primitivas que se consideran opacas en función de sus marcas de geometría e instancia.

Esta marca es mutuamente excluyente con RAY FLAG FORCE OPAQUE, RAY FLAG FORCE NON OPAQUE y \_ RAY FLAG \_ \_ \_ \_ \_ \_ \_ \_ CULL NON \_ \_ OPAQUE.


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY \_ FLAG \_ CULL \_ NON \_ OPAQUE**
</dt> <dd>

Anula todas las primitivas que se consideran no opacas en función de sus marcas de geometría e instancia.

Esta marca es mutuamente excluyente con RAY FLAG FORCE OPAQUE, RAY FLAG FORCE NON OPAQUE y \_ RAY FLAG \_ \_ \_ \_ \_ \_ \_ \_ CULL \_ OPAQUE.


</dd>

## <a name="requirements"></a>Requisitos



## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




