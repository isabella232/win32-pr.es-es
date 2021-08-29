---
title: Función D2DSampleInputAtOffset (D2d1effecthelpers.h)
description: Muestra la entrada N con un desplazamiento de desplazamiento de la coordenada de entrada. Solo está disponible para entradas complejas.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Función D2DSampleInputAtOffset Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e316e4daf533f66bba9d34a6ac89c61094db536e19e710d1c5c235edb7d250c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075309"
---
# <a name="d2dsampleinputatoffset-function"></a>Función D2DSampleInputAtOffset

Muestra la entrada N con un desplazamiento de desplazamiento de la coordenada de entrada. Solo está disponible para entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ en\]
</dt> <dd>

Número de entrada.

</dd> <dt>

*desplazamiento* \[ En\]
</dt> <dd>

Desplazamiento uv.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **float4**, con el formato TEXCOORDN.

## <a name="remarks"></a>Comentarios

En el ejemplo siguiente se muestra la función que se usa como parte de una máscara de degradado de resaltado y sombras.

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
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

 

 





