---
title: Función Texture2D::GetDimensions
description: Devuelve las dimensiones del recurso. | Función Texture2D::GetDimensions
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: 46eb5101dc119d2779f60d2e2b39a42c695933a5bffd477b407fea56c930038c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067705"
---
# <a name="texture2dgetdimensions-function"></a>Función Texture2D::GetDimensions

Devuelve las dimensiones del recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*MipLevel* \[ En\]
</dt> <dd>

Tipo: **uint**

Opcional. El nivel mipmap (debe especificarse si *se usa NumberOfLevels).*

</dd> <dt>

*Ancho* \[ out\]
</dt> <dd>

Tipo: **uint**

Ancho del recurso, en texturas.

</dd> <dt>

*Alto* \[ out\]
</dt> <dd>

Tipo: **uint**

Alto del recurso, en texturas.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **uint**

El número de niveles de asignación mip *(también requiere MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Comentarios

Esta es una lista de las versiones sobrecargadas de este método.


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




