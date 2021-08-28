---
title: Función Texture1DArray::GetDimensions
description: Devuelve las dimensiones del recurso. | Función Texture1DArray::GetDimensions
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 14a079443370f2363006ce23fcc5f5119b7ec7c48e3b15afe4969c989e071af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853325"
---
# <a name="texture1darraygetdimensions-function"></a>Función Texture1DArray::GetDimensions

Devuelve las dimensiones del recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*MipLevel* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opcional. Nivel de mapa mip (se debe especificar si *se usa NumberOfLevels).*

</dd> <dt>

*Ancho* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ancho del recurso, en texturas.

</dd> <dt>

*Elementos* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

El número de niveles de mapa mip *(también requiere MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta es una lista de las versiones sobrecargadas de este método.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
