---
description: Convierte una matriz de tipos Float de 32 bits en flotantes de 16 bits.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Función D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698361"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>Función D3DXFloat32To16Array (D3DX10Math. h)

Convierte una matriz de tipos Float de 32 bits en flotantes de 16 bits.

## <a name="syntax"></a>Sintaxis


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Puntero a la matriz de los flotantes de 16 bits.

</dd> <dt>

*código pIn* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntero a una matriz de floats de 32 bits.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Puntero a una matriz de flotantes de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
