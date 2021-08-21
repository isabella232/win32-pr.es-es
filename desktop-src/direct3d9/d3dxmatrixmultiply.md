---
description: 'Función D3DXMatrixMultiply (D3dx9math.h): determina el producto de dos matrices.'
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Función D3DXMatrixMultiply (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 64831287ab16f9b866ec5cd21b376fa190e8b42716453265875b2d8b5e7137d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122905"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a>Función D3DXMatrixMultiply (D3dx9math.h)

Determina el producto de dos matrices.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*pM1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.

</dd> <dt>

*pM2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el producto de dos matrices.

## <a name="remarks"></a>Comentarios

El resultado representa la transformación M1 seguida de la transformación M2 (Out = M1 \* M2).

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la **función D3DXMatrixMultiply** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




