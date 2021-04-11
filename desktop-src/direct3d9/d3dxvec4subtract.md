---
description: Resta dos vectores 4D.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: Función D3DXVec4Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1110930d8e37cf04f7de5129c2a72db4ecc4ac8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362826"
---
# <a name="d3dxvec4subtract-function"></a>D3DXVec4Subtract función)

Resta dos vectores 4D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Subtract(
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

Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.

</dd> <dt>

*pV2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es la diferencia de dos vectores.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec4Subtract** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Add**](d3dxvec3add.md)
</dt> <dt>

[**D3DXVec3Scale**](d3dxvec3scale.md)
</dt> </dl>

 

 




