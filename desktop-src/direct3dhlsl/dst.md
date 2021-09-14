---
title: Función dst
description: Calcula un vector de distancia. | Función dst
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- Función dst HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264191"
---
# <a name="dst-function"></a>Función dst

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

*src0* \[ En\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Primer vector.

</dd> <dt>

*src1* \[ En\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Segundo vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Vector de distancia calculado.

## <a name="remarks"></a>Observaciones

Esta función intrínseca proporciona la misma funcionalidad que la instrucción del sombreador de [vértices dst](dst---vs.md).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




