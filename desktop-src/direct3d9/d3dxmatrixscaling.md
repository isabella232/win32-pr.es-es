---
description: 'Función D3DXMatrixScaling (D3dx9math.h): crea una matriz que se escala a lo largo del eje X, el eje Y y el eje Z.'
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Función D3DXMatrixScaling (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ccd4cc6207bb211259833d163793c3499b51a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567840"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a>Función D3DXMatrixScaling (D3dx9math.h)

Crea una matriz que se escala a lo largo del eje X, el eje Y y el eje Z.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*sx* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de escalado que se aplica a lo largo del eje X.

</dd> <dt>

*sy* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de escalado que se aplica a lo largo del eje Y.

</dd> <dt>

*sz* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de escalado que se aplica a lo largo del eje Z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la transformación de escalado [**D3DXMATRIX**](d3dxmatrix.md).

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la **función D3DXMatrixScaling** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
