---
title: FUNCIÓN RWTexture2D::GetDimensions
description: Devuelve las dimensiones del recurso. | FUNCIÓN RWTexture2D::GetDimensions
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888188"
---
# <a name="rwtexture2dgetdimensions-function"></a>FUNCIÓN RWTexture2D::GetDimensions

Devuelve las dimensiones del recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta es una lista de las versiones sobrecargadas de este método.


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWTexture2D](sm5-object-rwtexture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
