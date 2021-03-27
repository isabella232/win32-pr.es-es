---
title: asdouble (función)
description: Reinterpreta un valor de conversión (valores de 2 32 bits) en un tipo Double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- función de dos funciones HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076901"
---
# <a name="asdouble-function"></a>asdouble (función)

Reinterpreta un valor de conversión (valores de 2 32 bits) en un tipo Double.

## <a name="syntax"></a>Sintaxis

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lowbits* \[ de\]
</dt> <dd>

Tipo: **uint**

Patrón de 32 bits bajo del valor de entrada.

</dd> <dt>

*highbits* \[ de\]
</dt> <dd>

Tipo: **uint**

El patrón de 32 bits alto del valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **Double**

La entrada (valores de 2 32 bits) se reconvierte como Double.

## <a name="remarks"></a>Observaciones

También está disponible la siguiente versión sobrecargada:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Si el valor de entrada es un componente de 2 32 bits, el tipo de valor devuelto contendrá un doble. Si el valor de entrada es un componente de 4 32 bits, el tipo de valor devuelto contendrá dos valores double. Si el valor de entrada es un tipo de 64 bits, el valor devuelto tendrá el mismo número de componentes que el valor de entrada.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




