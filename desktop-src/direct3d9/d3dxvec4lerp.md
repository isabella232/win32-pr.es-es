---
description: Realiza una interpolación lineal entre dos vectores 4D.
ms.assetid: a068a626-17cd-4df9-8f41-9b417bfda1d1
title: Función D3DXVec4Lerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8df6f7b4be5a39335532dc86096f989727230942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359367"
---
# <a name="d3dxvec4lerp-function"></a>Función D3DXVec4Lerp

Realiza una interpolación lineal entre dos vectores 4D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Lerp(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a la [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen.

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parámetro que interpola linealmente entre los vectores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la interpolación lineal.

## <a name="remarks"></a>Observaciones

Esta función realiza la interpolación lineal en función de la fórmula siguiente: V1 + s(V2-V1).

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec4Lerp** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
