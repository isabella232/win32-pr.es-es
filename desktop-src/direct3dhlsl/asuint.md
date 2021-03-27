---
title: asuint (función)
description: Reinterpreta el patrón de bits de un valor de 64 bits como dos enteros de 32 bits sin signo.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- función asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076900"
---
# <a name="asuint-function"></a>asuint (función)

Reinterpreta el patrón de bits de un valor de 64 bits como dos enteros de 32 bits sin signo.

## <a name="syntax"></a>Sintaxis

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **Double**

Valor de entrada.

</dd> <dt>

*lowbits* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

Patrón de *valor* de 32 bits bajo.

</dd> <dt>

*highbits* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

Modelo de *valor* de 32 bits alto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función es una versión alternativa del intrínseco [**asuint**](dx-graphics-hlsl-asuint.md) que está disponible en los modelos de sombreador anteriores y que se incorporó para el modelo de sombreador 5. La función original (reconocida en el compilador de HLSL por su firma diferente) sigue estando disponible para el modelo de sombreador 5.

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

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




