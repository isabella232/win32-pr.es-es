---
description: Devuelve un vector 2D que se forma con los componentes más pequeños de dos vectores 2D.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: Función D3DXVec2Minimize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1914ae9317d686e369f1cb2c7eb36ab54a29845f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060696"
---
# <a name="d3dxvec2minimize-function"></a>Función D3DXVec2Minimize

Devuelve un vector 2D que se forma con los componentes más pequeños de dos vectores 2D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que se conste de los componentes más pequeños de los dos vectores.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec2Minimize** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Maximize**](d3dxvec2maximize.md)
</dt> </dl>

 

 




