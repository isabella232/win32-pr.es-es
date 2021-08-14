---
title: FUNCIÓN RWTexture1D::GetDimensions
description: Devuelve las dimensiones del recurso. | FUNCIÓN RWTexture1D::GetDimensions
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
keywords:
- Función GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb779d071f471abe92b18ef456a2a016536a5231ccf327f8ebd175be8e5ff224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509297"
---
# <a name="rwtexture1dgetdimensions-function"></a>FUNCIÓN RWTexture1D::GetDimensions

Devuelve las dimensiones del recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ancho* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ancho del recurso, en texturas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Comentarios

Esta es una lista de las versiones sobrecargadas de este método.


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
