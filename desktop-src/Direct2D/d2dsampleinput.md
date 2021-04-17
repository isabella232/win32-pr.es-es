---
title: Función D2DSampleInput (D2d1effecthelpers. h)
description: Los ejemplos de entrada N en la posición UV. Solo está disponible para las entradas complejas.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681079"
---
# <a name="d2dsampleinput-function"></a>D2DSampleInput función)

Los ejemplos de entrada N en la posición UV. Solo está disponible para las entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Número de entrada.

</dd> <dt>

*UV* \[ de\]
</dt> <dd>

Posición UV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve una **FLOAT4**, en el formato TEXCOORDN.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra la función que se utiliza para calcular las normales de superficie.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Vinculación del sombreador de efectos](effect-shader-linking.md)
</dt> <dt>

[Aplicaciones auxiliares de HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





