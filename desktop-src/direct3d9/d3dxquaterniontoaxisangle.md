---
description: 'Función D3DXQuaternionToAxisAngle (D3dx9math.h): calcula el eje y el ángulo de rotación de un cuaternión.'
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Función D3DXQuaternionToAxisAngle (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b22b0a4c094a47e412172807c42cf25dc3c89342cf8e7e4ece9e731d9014bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731293"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>Función D3DXQuaternionToAxisAngle (D3dx9math.h)

Calcula el eje y el ángulo de rotación de un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQ* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Esta función devuelve un puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que identifica el eje de rotación del cuaternión.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Esta función devuelve un puntero a un valor FLOAT que identifica el ángulo de rotación del cuaternión en radianes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
