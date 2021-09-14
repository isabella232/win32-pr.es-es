---
description: Devuelve la longitud de un vector 3D.
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: Función D3DXVec3Length (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060684"
---
# <a name="d3dxvec3length-function"></a>Función D3DXVec3Length

Devuelve la longitud de un vector 3D.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud del vector.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
