---
title: 'Texture2D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture2D:: Getdimensions ((función)'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
keywords:
- Getdimensions (de función HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998181"
---
# <a name="texture2dgetdimensions-function"></a>Texture2D:: Getdimensions ((función)

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

*MipLevel* \[ de\]
</dt> <dd>

Tipo: **uint**

Opcional. Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).

</dd> <dt>

*Ancho* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

El ancho del recurso, en textura.

</dd> <dt>

*Alto* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

El alto del recurso, en textura.

</dd> <dt>

*NumberOfLevels* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

El número de niveles de mipmap (requiere también *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Observaciones

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



Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




