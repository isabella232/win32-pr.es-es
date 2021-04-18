---
description: Devuelve la longitud de un cuaternión.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: Función D3DXQuaternionLength (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424480"
---
# <a name="d3dxquaternionlength-function"></a>D3DXQuaternionLength función)

Devuelve la longitud de un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQ* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Longitud del cuaternión.

## <a name="remarks"></a>Observaciones

Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
