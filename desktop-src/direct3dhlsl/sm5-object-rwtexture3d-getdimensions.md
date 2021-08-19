---
title: Función RWTexture3D::GetDimensions
description: Devuelve las dimensiones del recurso. | Función RWTexture3D::GetDimensions
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 2fcd1f5e5fb1ab87193c2946e68a8144f34a7275c9ad90e87e9cc7e960336e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509213"
---
# <a name="rwtexture3dgetdimensions-function"></a>Función RWTexture3D::GetDimensions

Devuelve las dimensiones del recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ancho* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ancho del recurso, en texturas.

</dd> <dt>

*Alto* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Alto del recurso, en texturas.

</dd> <dt>

*Profundidad* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Profundidad del recurso, en los elementos de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta es una lista de las versiones sobrecargadas de este método.


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
