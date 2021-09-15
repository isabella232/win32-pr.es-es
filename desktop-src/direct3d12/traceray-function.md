---
description: Envía un rayo a una búsqueda de aciertos en una estructura de aceleración.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465547"
---
# <a name="traceray-function"></a>Función TraceRay

Envía un rayo a una búsqueda de aciertos en una estructura de aceleración.

## <a name="syntax"></a>Sintaxis
Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:

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



## <a name="parameters"></a>Parámetros

`AccelerationStructure`

Estructura de aceleración de nivel superior que se usará. Si se especifica una estructura de aceleración NULL, se fuerza una falta.

`RayFlags`

Combinación válida de [ray_flag](ray_flag.md) valores. El sistema solo propaga las marcas de rayo definidas, es decir, son visibles para el [sombreador RayFlags intrínsecos.](rayflags.md)

`InstanceInclusionMask`

Entero sin signo cuyos 8 bits inferiores se usan para incluir o rechazar instancias de geometry basadas en InstanceMask en cada instancia. Por ejemplo:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Entero sin signo que especifica el desplazamiento que se agregará a los cálculos de direccionamiento dentro de las tablas de sombreador para la indexación del grupo de pulsaciones.  Solo se usan los 4 bits inferiores de este valor.

`MultiplierForGeometryContributionToHitGroupIndex`

Entero sin signo que especifica el intervalo que se va a multiplicar por *GeometryContributionToHitGroupIndex*, que es solo el índice basado en 0 que la aplicación proporcionó a la geometría en su estructura de aceleración de nivel inferior. Solo se usan los 16 bits inferiores de este valor multiplicador.

`MissShaderIndex`

Entero sin signo que especifica el índice del sombreador miss dentro de una tabla de sombreador.

`Ray`

RayDesc [**que**](raydesc.md) representa el rayo del que se va a realizar el seguimiento.

`Payload`

Una carga de rayo definida por el usuario a la que se ha accedido tanto para la entrada como para la salida por los sombreadores invocados durante el raytracing.  Una [**vez completado TraceRay,**](traceray-function.md) el autor de la llamada también puede acceder a la carga.

## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




