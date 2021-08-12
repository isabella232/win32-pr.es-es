---
description: Devuelve la longitud de un vector 4D.
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: Función D3DXVec4Length (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 253f352016c042f9ddb310ebe0cbe4ac3af216b29963de4d30f91786b632b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297589"
---
# <a name="d3dxvec4length-function"></a>Función D3DXVec4Length

Devuelve la longitud de un vector 4D.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a la estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen.

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

[**D3DXVec4LengthSq**](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
