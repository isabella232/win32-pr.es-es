---
title: Función D2DSampleInput (D2d1effecthelpers.h)
description: Muestra la entrada N en la posición uv. Solo está disponible para entradas complejas.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Función D2DSampleInput Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163454"
---
# <a name="d2dsampleinput-function"></a>Función D2DSampleInput

Muestra la entrada N en la posición uv. Solo está disponible para entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ en\]
</dt> <dd>

Número de entrada.

</dd> <dt>

*uv* \[ En\]
</dt> <dd>

Posición uv.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **float4**, con el formato TEXCOORDN.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra la función que se usa para calcular las normales de la superficie.

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Vinculación del sombreador de efectos](effect-shader-linking.md)
</dt> <dt>

[Asistentes hlsl](hlsl-helpers.md)
</dt> </dl>

 

 





