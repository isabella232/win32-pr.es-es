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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072909"
---
# <a name="raydesc-structure"></a>Estructura RayDesc

Se pasa [**a la función TraceRay**](traceray-function.md) para definir el origen, la dirección y las extensiones del rayo.

## <a name="syntax"></a>Sintaxis


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>Campos

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**Origen**
</dt> <dd>

Origen del rayo.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**Tmin**
</dt> <dd>

La extensión mínima del rayo.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Dirección**
</dt> <dd>

Dirección del rayo.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**Tmax**
</dt> <dd>

Extensión máxima del rayo.


</dd>

## <a name="requirements"></a>Requisitos



## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




