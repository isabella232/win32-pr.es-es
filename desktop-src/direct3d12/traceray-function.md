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
# <a name="traceray-function"></a>Función TraceRay

Envía un rayo en una búsqueda de aciertos en una estructura de aceleración.

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

Estructura de aceleración de nivel superior que se va a usar. Si se especifica una estructura de aceleración nula, se fuerza una pérdida.

`RayFlags`

Combinación válida de valores de [ray_flag](ray_flag.md) . El sistema solo propaga las marcas de rayo definidas, es decir, que están visibles para el intrínseco del sombreador [RayFlags](rayflags.md) .

`InstanceInclusionMask`

Entero sin signo, los 8 bits inferiores de los cuales se usan para incluir o rechazar instancias de Geometry basadas en InstanceMask en cada instancia. Por ejemplo:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Entero sin signo que especifica el desplazamiento que se va a agregar en los cálculos de direccionamiento dentro de las tablas de sombreador para la indización del grupo de visitas.  Solo se usan los cuatro bits inferiores de este valor.

`MultiplierForGeometryContributionToHitGroupIndex`

Entero sin signo que especifica el intervalo que se va a multiplicar por *GeometryContributionToHitGroupIndex*, que es solo el índice de base 0 que la aplicación proporcionó la geometría en la estructura de aceleración de nivel inferior. Solo se usan los 16 bits inferiores de este valor de multiplicador.

`MissShaderIndex`

Entero sin signo que especifica el índice del sombreador de errores dentro de una tabla de sombreador.

`Ray`

[**RayDesc**](raydesc.md) que representa el rayo del que se va a realizar un seguimiento.

`Payload`

Una carga de rayo definida por el usuario a la que se tiene acceso tanto para la entrada como para la salida mediante sombreadores invocados durante raytracing.  Una vez finalizado [**TraceRay**](traceray-function.md) , el llamador puede tener acceso también a la carga.

## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)



## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




