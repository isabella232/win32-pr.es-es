---
description: 'Función D3DXFloat16To32Array (D3DX10Math.h): convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.'
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Función D3DXFloat16To32Array (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ae624fb05ce10447bd3b9082e171dc01224baaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113293"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>Función D3DXFloat16To32Array (D3DX10Math.h)

Convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a la matriz de flotantes de 32 bits.

</dd> <dt>

*pIn* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

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
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
