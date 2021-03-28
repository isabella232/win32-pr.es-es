---
title: DST (función)
description: Calcula un vector de distancia. | DST (función)
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- DST de la función HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914342"
---
# <a name="dst-function"></a>DST (función)

Calcula un vector de distancia.

## <a name="syntax"></a>Sintaxis

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*src0* \[ de\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Primer vector.

</dd> <dt>

*SRC1* \[ de\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Segundo vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Vector de distancia calculado.

## <a name="remarks"></a>Observaciones

Esta función intrínseca proporciona la misma funcionalidad que la instrucción [DST](dst---vs.md)del sombreador de vértices.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




