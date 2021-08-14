---
title: ddy_fine función
description: Calcula un derivado parcial de alta precisión con respecto a la coordenada x del espacio de pantalla. | ddy_fine función
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- ddy_fine hlsl
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b59f7ac500658570b19bf932e3abb042f9ecd8e27b63458c25032704c9ba4e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285888"
---
# <a name="ddy_fine-function"></a>Función ddy \_ fine

Calcula un derivado parcial de alta precisión con respecto a la coordenada x del espacio de pantalla.

## <a name="syntax"></a>Sintaxis

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **float**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **float**

Derivado parcial de alta precisión del *valor*.

## <a name="remarks"></a>Comentarios

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible. |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




