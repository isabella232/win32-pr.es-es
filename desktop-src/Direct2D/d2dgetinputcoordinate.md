---
title: Función D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Devuelve el valor de la TEXCOORDN de entrada. Solo está disponible para las entradas complejas.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Función D2DGetInputCoordinate Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681018"
---
# <a name="d2dgetinputcoordinate-function"></a>D2DGetInputCoordinate función)

Devuelve el valor de la TEXCOORDN de entrada. Solo está disponible para las entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Número de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve una **FLOAT4**, en el formato TEXCOORDN.

## <a name="remarks"></a>Observaciones

La coordenada devuelta por esta función está en el espacio textura. Un sombreador no debe tomar ninguna dependencia sobre cómo se calcula este valor. Solo debe usarlo para muestrear la entrada del sombreador de píxeles. Para obtener más información, vea [Agregar un sombreador de píxeles a una transformación personalizada](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).

En el ejemplo siguiente se muestra la función utilizada para un efecto de mapa de desplazamiento.

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
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

 

