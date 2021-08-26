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
ms.openlocfilehash: d8b0d8112902486102e6a4338445a2526b23cab8dafb2ea8b7d68b87d5b803af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068345"
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

## <a name="remarks"></a>Comentarios

Esta función intrínseca proporciona la misma funcionalidad que la instrucción del sombreador de [vértices dst](dst---vs.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




