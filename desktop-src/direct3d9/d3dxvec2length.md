---
description: Devuelve la longitud de un vector 2D.
ms.assetid: 376fd2ca-c89d-41e7-a15c-a79d7281d010
title: Función D3DXVec2Length (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bddfbb617b05212b04977965fc4d9497df8b839757aa137e43962072f3ed2226
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676055"
---
# <a name="d3dxvec2length-function"></a>Función D3DXVec2Length

Devuelve la longitud de un vector 2D.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXVec2Length(
  _In_ const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a la estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud del vector.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2LengthSq**](d3dxvec2lengthsq.md)
</dt> </dl>

 

 
