---
title: 'Texture1DArray:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture1DArray:: Getdimensions ((función)'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820706"
---
# <a name="texture1darraygetdimensions-function"></a>Texture1DArray:: Getdimensions ((función)

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

*MipLevel* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opcional. Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).

</dd> <dt>

*Ancho* \[ de enuncia\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El ancho del recurso, en textura.

</dd> <dt>

*Elementos* \[ de enuncia\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

</dd> <dt>

*NumberOfLevels* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El número de niveles de mipmap (requiere también *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

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



Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
