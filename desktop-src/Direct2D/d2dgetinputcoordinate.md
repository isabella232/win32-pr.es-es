---
title: Función D2DGetInputCoordinate (D2d1effecthelpers.h)
description: Devuelve el valor de la entrada TEXASCOORDN. Solo está disponible para entradas complejas.
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
ms.openlocfilehash: 5a3fe0d825dea70c8e5211b8c13f1e850fa513670bbc93de98f1f8e2b87ef046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075299"
---
# <a name="d2dgetinputcoordinate-function"></a>Función D2DGetInputCoordinate

Devuelve el valor de la entrada TEXASCOORDN. Disponible solo para entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ en\]
</dt> <dd>

Número de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **un valor float4**, con el formato TEXCOORDN.

## <a name="remarks"></a>Comentarios

La coordenada devuelta por esta función está en el espacio de textura. Un sombreador no debe tener dependencias de cómo se calcula este valor. Solo se debe usar para muestrear la entrada del sombreador de píxeles. Para obtener más información, vea [Agregar un sombreador de píxeles a una transformación personalizada.](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform)

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

[Asistentes hlsl](hlsl-helpers.md)
</dt> </dl>

 

