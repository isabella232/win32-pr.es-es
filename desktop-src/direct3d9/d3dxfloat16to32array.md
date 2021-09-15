---
description: 'Función D3DXFloat16To32Array (D3dx9math.h): convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.'
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Función D3DXFloat16To32Array (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567949"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>Función D3DXFloat16To32Array (D3dx9math.h)

Convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a la matriz de flotantes de 32 bits.

</dd> <dt>

*pIn* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Puntero a una matriz de flotantes de 16 bits.

</dd> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de flotantes de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
