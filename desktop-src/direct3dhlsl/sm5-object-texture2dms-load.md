---
title: Función Texture2DMS::Load(int,int)
description: Obtiene un valor. | Función Texture2DMS::Load(int,int)
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Carga de la función DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0997a1bd30b4912864674015057fcafec227d90ad05b16b88fd3f05b671f155c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285733"
---
# <a name="texture2dmsloadintint-function"></a>Función Texture2DMS::Load(int,int)

Obtiene un valor.

## <a name="syntax"></a>Sintaxis

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*coord* \[ En\]
</dt> <dd>

Tipo: **int2**

Ubicación de entrada.

</dd> <dt>

*sampleindex* \[ En\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Índice de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **T**

Un valor, cuyo tipo coincide con el tipo de plantilla de textura.

## <a name="remarks"></a>Comentarios

Esta es una lista de las versiones sobrecargadas de este método.


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos de carga](texture2dms-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
