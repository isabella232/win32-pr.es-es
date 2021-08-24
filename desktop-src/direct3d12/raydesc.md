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
ms.openlocfilehash: a4fa44e68e8747a0a8366ca2d949290f585d4b70d9e75b4ed2d3b6fdda0d05c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123690"
---
# <a name="raydesc-structure"></a>Estructura RayDesc

Se pasa a [**la función TraceRay**](traceray-function.md) para definir el origen, la dirección y las extensiones del rayo.

## <a name="syntax"></a>Syntax


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

Extensión mínima del rayo.


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

 

 




