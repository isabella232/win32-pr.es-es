---
title: 'Texture2DMSArray:: Load (int, int) (función)'
description: 'Obtiene un valor. | Texture2DMSArray:: Load (int, int) (función)'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003711"
---
# <a name="texture2dmsarrayloadintint-function"></a>Texture2DMSArray:: Load (int, int) (función)

Obtiene un valor.

## <a name="syntax"></a>Sintaxis

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*coordenadas* \[ de\]
</dt> <dd>

Tipo: **INT3**

Ubicación de entrada.

</dd> <dt>

*sampleindex* \[ de\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Índice de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **T**

Un valor, cuyo tipo coincide con el tipo de plantilla de textura.

## <a name="remarks"></a>Observaciones

Esta es una lista de las versiones sobrecargadas de este método.


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Cargar métodos](texture2dmsarray-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
