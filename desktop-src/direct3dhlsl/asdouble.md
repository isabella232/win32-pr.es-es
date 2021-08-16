---
title: Función asdouble
description: Reinterpreta un valor de conversión (dos valores de 32 bits) en un valor double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- Función asdouble HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e191a2bf9ee7fb46337c3c7dfef7f8dea3525acf936ab745c07e7720f1ac509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626645"
---
# <a name="asdouble-function"></a>Función asdouble

Reinterpreta un valor de conversión (dos valores de 32 bits) en un valor double.

## <a name="syntax"></a>Sintaxis

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lowbits* \[ En\]
</dt> <dd>

Tipo: **uint**

Patrón de 32 bits bajo del valor de entrada.

</dd> <dt>

*highbits* \[ En\]
</dt> <dd>

Tipo: **uint**

Patrón alto de 32 bits del valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **double**

La entrada (dos valores de 32 bits) se vuelve a convertir como doble.

## <a name="remarks"></a>Comentarios

También está disponible la siguiente versión sobrecargada:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Si el valor de entrada es de dos componentes de 32 bits, el tipo de valor devuelto contendrá un valor double. Si el valor de entrada es de cuatro componentes de 32 bits, el tipo de valor devuelto contendrá dos valores double. Si el valor de entrada es de 64 bits, el valor devuelto tendrá el mismo número de componentes que el valor de entrada.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




