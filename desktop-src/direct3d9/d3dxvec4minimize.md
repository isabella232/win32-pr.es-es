---
description: Devuelve un vector 4D que se conste de los componentes más pequeños de dos vectores 4D.
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: Función D3DXVec4Minimize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969723"
---
# <a name="d3dxvec4minimize-function"></a>Función D3DXVec4Minimize

Devuelve un vector 4D que se conste de los componentes más pequeños de dos vectores 4D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que se conste de los componentes más pequeños de los dos vectores.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec4Minimize** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Maximize**](d3dxvec4maximize.md)
</dt> </dl>

 

 




